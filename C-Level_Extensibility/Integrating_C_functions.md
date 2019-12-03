## Integrating C functions

The C-level extensibility mechanism lets you implement Flash extensibility files using a combination of JavaScript and C code.
***Note:** Adobe Animate runs on 64-bit operating systems only. All C extensions for this release must be built (or rebuilt) for 64 bit support.*
The process for implementing this capability is summarized in the following steps:

1.  Define functions using the C or C++ language.

2.  Bundle them in a DLL file (Windows) or a shared library (Macintosh).

3.  Save the DLL file or library in the appropriate location:

    -   Windows 7 and 8:

*boot drive*\\Users\\*username*\\AppData\\Local\\Adobe\\Flash *CC*\\*language*\\Configuration\\External Libraries

-   Mac OS X:

Macintosh HD/Users/*username*/Library/Application Support/Adobe/Flash
*CC*/*language*/Configuration/External Libraries

1.  Create a JSFL file that calls the functions.

2.  Run the JSFL file from the Commands menu in the Flash authoring environment. For more information, see ["Sample DLL implementation" on page 595](#sample-dll-implementation).

### C-level extensibility and the JavaScript interpreter

The C code in the DLL or shared library interacts with the Animate JavaScript API at three different times:

-   At startup, to register the library’s functions

-   When the C function is called, to unpack the arguments that are being passed from JavaScript to C

-   Before the C function returns, to package the return value

To accomplish these tasks, the interpreter defines several data types and exposes an API. Definitions for the data types and functions that are listed in this section appear in the mm\_jsapi.h file. For your library to work properly, you must include the mm\_jsapi.h file at the top of each file in your library, with the following line:
\#include "mm\_jsapi.h"
Including the mm\_jsapi.h file includes the mm\_jsapi\_environment.h file, which defines the MM\_Environment structure.
To get a copy of the mm\_jsapi.h file, extract it from the sample ZIP or SIT file (see ["Sample DLL implementation" on](#sample-dll-implementation) [page 595](#sample-dll-implementation)), or copy the following code into a file that you name mm\_jsapi.h:
\#ifndef \_MM\_JSAPI\_H\_ \#define \_MM\_JSAPI\_H\_
/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\* Public data types
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*/
typedef struct JSContext JSContext; typedef struct JSObject JSObject; typedef long jsval;
\#ifndef JSBool typedef long JSBool; \#endif
typedef JSBool (\*JSNative)(JSContext \*cx, JSObject \*obj, unsigned int argc, jsval \*argv, jsval \*rval);
/\* Possible values for JSBool \*/ \#define JS\_TRUE 1
\#define JS\_FALSE 0
/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\* Public functions
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*/
/\* JSBool JS\_DefineFunction(unsigned short \*name, JSNative call, unsigned int nargs) \*/ \#define JS\_DefineFunction(n, c, a) \\
(mmEnv.defineFunction ? (\*(mmEnv.defineFunction))(mmEnv.libObj, n, c, a) \\
: JS\_FALSE)
/\* unsigned short \*JS\_ValueToString(JSContext \*cx, jsval v, unsigned int \*pLength) \*/ \#define JS\_ValueToString(c, v, l) \\
(mmEnv.valueToString? (\*(mmEnv.valueToString))(c, v, l) : (char \*)0)
/\* unsigned char \*JS\_ValueToBytes(JSContext \*cx, jsval v, unsigned int \*pLength) \*/ \#define JS\_ValueToBytes(c, v, l) \\
(mmEnv.valueToBytes? (\*(mmEnv.valueToBytes))(c, v, l) : (unsigned char \*)0)
/\* JSBool JS\_ValueToInteger(JSContext \*cx, jsval v, long \*lp); \*/ \#define JS\_ValueToInteger(c, v, l) \\
(mmEnv.valueToInteger ? (\*(mmEnv.valueToInteger))(c, v, l) : JS\_FALSE)
/\* JSBool JS\_ValueToDouble(JSContext \*cx, jsval v, double \*dp); \*/ \#define JS\_ValueToDouble(c, v, d) \\
(mmEnv.valueToDouble? (\*(mmEnv.valueToDouble))(c, v, d) : JS\_FALSE)
/\* JSBool JS\_ValueToBoolean(JSContext \*cx, jsval v, JSBool \*bp); \*/ \#define JS\_ValueToBoolean(c, v, b) \\
(mmEnv.valueToBoolean ? (\*(mmEnv.valueToBoolean))(c, v, b) : JS\_FALSE)
/\* JSBool JS\_ValueToObject(JSContext \*cx, jsval v, JSObject \*\*op); \*/ \#define JS\_ValueToObject(c, v, o) \\
(mmEnv.valueToObject? (\*(mmEnv.valueToObject))(c, v, o) : JS\_FALSE)
/\* JSBool JS\_StringToValue(JSContext \*cx, unsigned short \*bytes, uint sz, jsval \*vp); \*/ \#define JS\_StringToValue(c, b, s, v) \\
(mmEnv.stringToValue? (\*(mmEnv.stringToValue))(c, b, s, v) : JS\_FALSE)
/\* JSBool JS\_BytesToValue(JSContext \*cx, unsigned char \*bytes, uint sz, jsval \*vp); \*/ \#define JS\_BytesToValue(c, b, s, v) \\
(mmEnv.bytesToValue? (\*(mmEnv.bytesToValue))(c, b, s, v) : JS\_FALSE)
/\* JSBool JS\_DoubleToValue(JSContext \*cx, double dv, jsval \*vp); \*/ \#define JS\_DoubleToValue(c, d, v) \\
(mmEnv.doubleToValue? (\*(mmEnv.doubleToValue))(c, d, v) : JS\_FALSE)
/\* jsval JS\_IntegerToValue(long lv); \*/
\#define JS\_IntegerToValue(lv) (((jsval)(lv) \<\< 1) \| 0x1)
/\* jsval JS\_BooleanToValue(JSBool bv); \*/
\#define JS\_BooleanToValue(bv) (((jsval)(bv) \<\< 3) \| 0x6)
/\* jsval JS\_ObjectToValue(JSObject \*obj); \*/ \#define JS\_ObjectToValue(ov)((jsval)(ov))
/\* unsigned short \*JS\_ObjectType(JSObject \*obj); \*/ \#define JS\_ObjectType(o) \\
(mmEnv.objectType ? (\*(mmEnv.objectType))(o) : (char \*)0)
/\* JSObject \*JS\_NewArrayObject(JSContext \*cx, unsigned int length, jsval \*v) \*/ \#define JS\_NewArrayObject(c, l, v) \\
(mmEnv.newArrayObject ? (\*(mmEnv.newArrayObject))(c, l, v) : (JSObject \*)0)
/\* long JS\_GetArrayLength(JSContext \*cx, JSObject \*obj) \*/ \#define JS\_GetArrayLength(c, o) \\
(mmEnv.getArrayLength ? (\*(mmEnv.getArrayLength))(c, o) : -1)
/\* JSBool JS\_GetElement(JSContext \*cx, JSObject \*obj, jsint idx, jsval \*vp) \*/ \#define JS\_GetElement(c, o, i, v) \\
(mmEnv.getElement ? (\*(mmEnv.getElement))(c, o, i, v) : JS\_FALSE)
/\* JSBool JS\_SetElement(JSContext \*cx, JSObject \*obj, jsint idx, jsval \*vp) \*/ \#define JS\_SetElement(c, o, i, v) \\
(mmEnv.setElement ? (\*(mmEnv.setElement))(c, o, i, v) : JS\_FALSE)
/\* JSBool JS\_ExecuteScript(JSContext \*cx, JSObject \*obj, unsigned short \*script,
\* unsigned int sz, jsval \*rval) \*/ \#define JS\_ExecuteScript(c, o, s, z, r) \\
(mmEnv.executeScript? (\*(mmEnv.executeScript))(c, o, s, z, (LPCTSTR) <span class="underline"</spanFILE <span class="underline"</span, \\
<span class="underline"</spanLINE <span class="underline"</span, r) : JS\_FALSE)
/\* JSBool JS\_ReportError(JSContext \*cx, unsigned short \*error, unsigned int sz) \*/ \#define JS\_ReportError(c, e, s) \\
(mmEnv.reportError? (\*(mmEnv.reportError))(c, e, s) : JS\_FALSE)
/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
\* Private data types, macros, and globals
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*/
typedef struct { JSObject \*libObj;
JSBool (\*defineFunction)(JSObject \*libObj, unsigned short \*name, JSNative call, unsigned int nargs);
unsigned short \*(\*valueToString)(JSContext \*cx, jsval v, unsigned int \*pLength); unsigned char \*(\*valueToBytes)(JSContext \*cx, jsval v, unsigned int \*pLength); JSBool (\*valueToInteger)(JSContext \*cx, jsval v, long \*lp);
JSBool (\*valueToDouble)(JSContext \*cx, jsval v, double \*dp); JSBool (\*valueToBoolean)(JSContext \*cx, jsval v, JSBool \*bp); JSBool (\*valueToObject)(JSContext \*cx, jsval v, JSObject \*\*op);
JSBool (\*stringToValue)(JSContext \*cx, unsigned short \*b, unsigned int sz, jsval \*vp); JSBool (\*bytesToValue)(JSContext \*cx, unsigned char \*b, unsigned int sz, jsval \*vp); JSBool (\*doubleToValue)(JSContext \*cx, double dv, jsval \*vp);
unsigned short \*(\*objectType)(JSObject \*obj);
JSObject \*(\*newArrayObject)(JSContext \*cx, unsigned int length, jsval \*vp); long (\*getArrayLength)(JSContext \*cx, JSObject \*obj);
JSBool (\*getElement)(JSContext \*cx, JSObject \*obj, unsigned int idx, jsval \*vp);
JSBool (\*setElement)(JSContext \*cx, JSObject \*obj, unsigned int idx, jsval \*vp);
JSBool (\*executeScript)(JSContext \*cx, JSObject \*obj, unsigned short \*script, unsigned int sz, unsigned short \*file, unsigned int lineNum, jsval \*rval); JSBool (\*reportError)(JSContext \*cx, unsigned short \*error, unsigned int sz);
} MM\_Environment;
extern MM\_Environment mmEnv;
// Declare the external entry point and linkage \#ifdef \_WIN32
\# ifndef \_MAC
// Windows
<span class="underline"</spandeclspec( dllexport ) void MM\_InitWrapper( MM\_Environment \*env, unsigned int envSize ); \# endif
\#else
extern void MM\_InitWrapper( MM\_Environment \*env, unsigned int envSize ); \#endif
\#define MM\_STATE\\
/\* Definitions of global variables \*/ \\ MM\_Environment mmEnv; \\
\\ void\\
MM\_InitWrapper(MM\_Environment \*env, unsigned int envSize) \\
{ \\
extern void MM\_Init();\\
\\
char \*\*envPtr = (char \*\*)env; \\ char \*\*mmPtr =(char \*\*)(&mmEnv);\\
char \*\*envEnd = (char \*\*)((char \*)envPtr + envSize);\\
char \*\*mmEnd =(char \*\*)((char \*)mmPtr+ sizeof(MM\_Environment)); \\
\\
/\* Copy fields from env to mmEnv, one pointer at a time \*/\\ while (mmPtr \< mmEnd && envPtr \< envEnd)\\
\*mmPtr++ = \*envPtr++; \\
\\
/\* If env doesn't define all of mmEnv's fields, set extras to NULL \*/ \\ while (mmPtr \< mmEnd) \\
\*mmPtr++ = (char \*)0; \\
\\
/\* Call user's MM\_Init function \*/\\ MM\_Init();\\
} \\
\#endif /\* \_MM\_JSAPI\_H\_ \*/

### Sample DLL implementation

This section illustrates how to build a simple DLL implementation. If you want to see how the process works without actually building the DLL yourself, you can install the sample DLL files that are provided in the Samples.zip file; the files are located in the ExtendingFlash/dllSampleComputeSum folder. (For information on downloading the Samples.zip file, see ["Sample implementations" on page 16](#_bookmark9).) Extract the sample files from the dllSampleComputeSum.dmg or dllSampleComputeSum.zip file, and then do the following:

-   Store the Sample.jsfl file in the Configuration/Commands directory (see ["Saving JSFL files" on page 2](#_bookmark3)).

-   Store the Sample.dll file in the Configuration/External Libraries directory (see ["Integrating C functions" on page 591](#_bookmark1167)).

-   In the Flash authoring environment, select Commands \Sample. The trace statement in the JSFL file sends the results of the function defined in Sample.dll to the Output panel.

The rest of this section discusses the development of the sample. In this case, the DLL contains only one function, which adds two numbers. The C code is shown in the following example:
// Source code in C
// Save the DLL or shared library with the name "Sample". \#include \<windows.h\>
\#include \<stdlib.h\\#include "mm\_jsapi.h"
// A sample function
// Every implementation of a JavaScript function must have this signature.
JSBool computeSum(JSContext \*cx, JSObject \*obj, unsigned int argc, jsval \*argv, jsval \*rval)
{
long a, b, sum;
// Make sure the right number of arguments were passed in. if (argc != 2)
return JS\_FALSE;
// Convert the two arguments from jsvals to longs.
if (JS\_ValueToInteger(cx, argv\[0\], &a) == JS\_FALSE \|\| JS\_ValueToInteger(cx, argv\[1\], &b) == JS\_FALSE)
return JS\_FALSE;
/\* Perform the actual work. \*/ sum = a + b;
/\* Package the return value as a jsval. \*/
\*rval = JS\_IntegerToValue(sum);
/\* Indicate success. \*/ return JS\_TRUE;
}
After writing this code, build the DLL file or shared library, and store it in the appropriate Configuration/External Libraries directory (see ["Integrating C functions" on page 591](#_bookmark1167)). Then create a JSFL file with the following code, and store it in the Configuration/Commands directory (see ["Saving JSFL files" on page 2](#_bookmark3)).
// JSFL file to run C function defined above. var a = 5;
var b = 10;
var sum = Sample.computeSum(a, b);
fl.trace("The sum of " + a + " and " + b + " is " + sum );
To run the function defined in the DLL, select Commands \Sample in the Flash authoring environment.

