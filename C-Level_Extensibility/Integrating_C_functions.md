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

2.  Run the JSFL file from the Commands menu in the Flash authoring environment. For more information, see ["Sample DLL implementation" on page 595](../C-Level_Extensibility/Integrating_C_functions.md).

### C-level extensibility and the JavaScript interpreter

The C code in the DLL or shared library interacts with the Flash JavaScript API at three different times:

-   At startup, to register the library’s functions

-   When the C function is called, to unpack the arguments that are being passed from JavaScript to C

-   Before the C function returns, to package the return value

To accomplish these tasks, the interpreter defines several data types and exposes an API. Definitions for the data types and functions that are listed in this section appear in the mm_jsapi.h file. For your library to work properly, you must include the mm_jsapi.h file at the top of each file in your library, with the following line:

*#include "mm_jsapi.h"*

Including the mm_jsapi.h file includes the mm_jsapi_environment.h file, which defines the MM_Environment structure.

To get a copy of the mm_jsapi.h file, extract it from the sample ZIP or SIT file (see ["Sample DLL implementation" on](../C-Level_Extensibility/Integrating_C_functions.md) [page 595](../C-Level_Extensibility/Integrating_C_functions.md)), or copy the following code into a file that you name mm_jsapi.h:

```javascript
#ifndef _MM_JSAPI_H_ 

#define _MM_JSAPI_H_

/***************************************************************************

* Public data types

****************************************************************************/

typedef struct JSContext JSContext; 
typedef struct JSObject JSObject; 
ypedef long jsval;
#ifndef JSBool 
typedef long JSBool; 
#endif

typedef JSBool (*JSNative)(JSContext *cx, JSObject *obj, unsigned int argc, jsval *argv, jsval *rval);

/* Possible values for JSBool */ 
#define JS_TRUE 1
#define JS_FALSE 0

/***************************************************************************

* Public Function

****************************************************************************/

/* JSBool JS_DefineFunction(unsigned short *name, JSNative call, unsigned int nargs) */ 
#define JS_DefineFunction(n, c, a) \
(mmEnv.defineFunction ? (*(mmEnv.defineFunction))(mmEnv.libObj, n, c, a) \
: JS_FALSE)

/* unsigned short *JS_ValueToString(JSContext *cx, jsval v, unsigned int *pLength) */ 
#define JS_ValueToString(c, v, l) \
(mmEnv.valueToString? (*(mmEnv.valueToString))(c, v, l) : (char \*)0)


/* unsigned char *JS_ValueToBytes(JSContext *cx, jsval v, unsigned int *pLength) */ 
#define JS_ValueToBytes(c, v, l) \
(mmEnv.valueToBytes? (*(mmEnv.valueToBytes))(c, v, l) : (unsigned char *)0)


/* JSBool JS_ValueToInteger(JSContext *cx, jsval v, long *lp); */ 
#define JS_ValueToInteger(c, v, l) \
(mmEnv.valueToInteger ? (*(mmEnv.valueToInteger))(c, v, l) : JS_FALSE)


/* JSBool JS_ValueToDouble(JSContext *cx, jsval v, double *dp); */ 
#define JS_ValueToDouble(c, v, d) \
(mmEnv.valueToDouble? (*(mmEnv.valueToDouble))(c, v, d) : JS_FALSE)


/* JSBool JS_ValueToBoolean(JSContext *cx, jsval v, JSBool *bp); */ 
#define JS_ValueToBoolean(c, v, b) \
(mmEnv.valueToBoolean ? (*(mmEnv.valueToBoolean))(c, v, b) : JS_FALSE)


/* JSBool JS_ValueToObject(JSContext *cx, jsval v, JSObject **op); */ 
#define JS_ValueToObject(c, v, o) \
(mmEnv.valueToObject? (*(mmEnv.valueToObject))(c, v, o) : JS_FALSE)


/* JSBool JS_StringToValue(JSContext *cx, unsigned short *bytes, uint sz, jsval *vp); */ 
#define JS_StringToValue(c, b, s, v) \
(mmEnv.stringToValue? (*(mmEnv.stringToValue))(c, b, s, v) : JS_FALSE)


/* JSBool JS_BytesToValue(JSContext *cx, unsigned char *bytes, uint sz, jsval *vp); */ 
#define JS_BytesToValue(c, b, s, v) \
(mmEnv.bytesToValue? (*(mmEnv.bytesToValue))(c, b, s, v) : JS_FALSE)

/* JSBool JS_DoubleToValue(JSContext *cx, double dv, jsval *vp); */ 
#define JS_DoubleToValue(c, d, v) \
(mmEnv.doubleToValue? (*(mmEnv.doubleToValue))(c, d, v) : JS_FALSE)


/* jsval JS_IntegerToValue(long lv); */
#define JS_IntegerToValue(lv) (((jsval)(lv) \<\< 1) \| 0x1)


/* jsval JS_BooleanToValue(JSBool bv); */
#define JS_BooleanToValue(bv) (((jsval)(bv) \<\< 3) \| 0x6)


/* jsval JS_ObjectToValue(JSObject *obj); */ 
#define JS_ObjectToValue(ov)((jsval)(ov))


/* unsigned short *JS_ObjectType(JSObject *obj); */ 
#define JS_ObjectType(o) \
(mmEnv.objectType ? (*(mmEnv.objectType))(o) : (char *)0)


/* JSObject *JS_NewArrayObject(JSContext *cx, unsigned int length, jsval *v) */
#define JS_NewArrayObject(c, l, v) \
(mmEnv.newArrayObject ? (*(mmEnv.newArrayObject))(c, l, v) : (JSObject *)0)


/* long JS_GetArrayLength(JSContext *cx, JSObject *obj) */ 
#define JS_GetArrayLength(c, o) \
(mmEnv.getArrayLength ? (*(mmEnv.getArrayLength))(c, o) : -1)


/* JSBool JS_GetElement(JSContext *cx, JSObject *obj, jsint idx, jsval *vp) */
#define JS_GetElement(c, o, i, v) \
(mmEnv.getElement ? (*(mmEnv.getElement))(c, o, i, v) : JS_FALSE)


/* JSBool JS_SetElement(JSContext *cx, JSObject *obj, jsint idx, jsval *vp) */
#define JS_SetElement(c, o, i, v) \
(mmEnv.setElement ? (*(mmEnv.setElement))(c, o, i, v) : JS_FALSE)


/* JSBool JS_ExecuteScript(JSContext *cx, JSObject *obj, *unsigned short *script,
*unsigned int sz, jsval *rval) */ 
#define JS_ExecuteScript(c, o, s, z, r) \
(mmEnv.executeScript? (*(mmEnv.executeScript))(c, o, s, z, (LPCTSTR)__FILE__, \  __LINE__, r) : JS_FALSE)  


/* JSBool JS_ReportError(JSContext *cx, unsigned short *error, unsigned int sz) */ 
#define JS_ReportError(c, e, s) \
(mmEnv.reportError? (*(mmEnv.reportError))(c, e, s) : JS_FALSE)



/***************************************************************************

* Private data types, macros, and globals

****************************************************************************/ 

typedef struct { 
    JSObject *libObj;
    JSBool (*defineFunction)(JSObject *libObj, unsigned short *name, JSNative call, unsigned int nargs);
    unsigned short *(*valueToString)(JSContext *cx, jsval v, unsigned int *pLength); 
    unsigned char *(*valueToBytes)(JSContext *cx, jsval v, unsigned int *pLength); 
    JSBool (*valueToInteger)(JSContext *cx, jsval v, long *lp);
    JSBool (*valueToDouble)(JSContext *cx, jsval v, double *dp); 
    JSBool (*valueToBoolean)(JSContext *cx, jsval v, JSBool *bp); 
    JSBool (*valueToObject)(JSContext *cx, jsval v, JSObject **op);
    JSBool (*stringToValue)(JSContext *cx, unsigned short *b, unsigned int sz, jsval *vp); 
    JSBool (*bytesToValue)(JSContext *cx, unsigned char *b, unsigned int sz, jsval *vp); 
    JSBool (*doubleToValue)(JSContext *cx, double dv, jsval *vp);
    unsigned short *(*objectType)(JSObject *obj);
    JSObject *(*newArrayObject)(JSContext *cx, unsigned int length, jsval *vp); 
    long (*getArrayLength)(JSContext *cx, JSObject *obj);
    JSBool (*getElement)(JSContext *cx, JSObject *obj, unsigned int idx, jsval *vp);
    JSBool (*setElement)(JSContext *cx, JSObject *obj, unsigned int idx, jsval *vp);
    JSBool (*executeScript)(JSContext *cx, JSObject *obj, unsigned short *script, unsigned int sz, unsigned short *file, unsigned int lineNum, jsval *rval); 
    JSBool (*reportError)(JSContext *cx, unsigned short *error, unsigned int sz);
} MM_Environment;

extern MM_Environment mmEnv;

// Declare the external entry point and linkage 
#ifdef _WIN32
# ifndef _MAC
// Windows
__declspec ( dllexport ) void MM_InitWrapper( MM_Environment *env, unsigned int envSize ); 
# endif
#else
extern void MM_InitWrapper( MM_Environment *env, unsigned int envSize ); 
#endif


#define MM_STATE\
/* Definitions of global variables */ 
\ MM_Environment mmEnv; \
\ void\
MM_InitWrapper(MM_Environment *env, unsigned int envSize) \
{ \
extern void MM_Init();\
\
char **envPtr = (char **)env; \
 char **mmPtr =(char **)(&mmEnv);\
 char **envEnd = (char **)((char *)envPtr + envSize);\
 char **mmEnd =(char **)((char *)mmPtr+ sizeof(MM_Environment)); \
\
/* Copy fields from env to mmEnv, one pointer at a time */\ 
while (mmPtr < mmEnd && envPtr < envEnd)\
*mmPtr++ = *envPtr++; \
\
/* If env doesn't define all of mmEnv's fields, set extras to NULL */ \ 
while (mmPtr < mmEnd) \
*mmPtr++ = (char *)0; \
\
/* Call user's MM_Init function */\
MM_Init();\
} \

#endif /* _MM_JSAPI_H_ */
```

### Sample DLL implementation

This section illustrates how to build a simple DLL implementation. If you want to see how the process works without actually building the DLL yourself, you can install the sample DLL files that are provided in the Samples.zip file; the files are located in the ExtendingFlash/dllSampleComputeSum folder. (For information on downloading the Samples.zip file, see ["Sample implementations" on page 16](../C-Level_Extensibility/Integrating_C_functions.md) Extract the sample files from the dllSampleComputeSum.dmg or dllSampleComputeSum.zip file, and then do the following:

-   Store the Sample.jsfl file in the Configuration/Commands directory (see ["Saving JSFL files" on page 2](../Introduction/Working_with_the_JavaScript_API.md).

-   Store the Sample.dll file in the Configuration/External Libraries directory (see ["Integrating C functions" on page 591](../C-Level_Extensibility/Integrating_C_functions.md)).

-   In the Flash authoring environment, select Commands >Sample. The trace statement in the JSFL file sends the results of the function defined in Sample.dll to the Output panel.

The rest of this section discusses the development of the sample. In this case, the DLL contains only one function, which adds two numbers. The C code is shown in the following example:

```javascript
// Source code in C
// Save the DLL or shared library with the name "Sample". 
#include <windows.h>
#include <stdlib.h>
#include "mm_jsapi.h"
// A sample function
// Every implementation of a JavaScript function must have this signature.
JSBool computeSum(JSContext *cx, JSObject *obj, unsigned int argc, jsval *argv, jsval *rval)
{
    long a, b, sum;

    // Make sure the right number of arguments were passed in. 
    if (argc != 2)
    return JS_FALSE;

    // Convert the two arguments from jsvals to longs.
    if (JS_ValueToInteger(cx, argv[0], &a) == JS_FALSE || 
        JS_ValueToInteger(cx, argv[1], &b) == JS_FALSE)
            return JS_FALSE;

    /* Perform the actual work. */ 
    sum = a + b;

    /* Package the return value as a jsval. */
    *rval = JS_IntegerToValue(sum);

    /* Indicate success. */ 
    return JS_TRUE;
}
```
After writing this code, build the DLL file or shared library, and store it in the appropriate Configuration/External Libraries directory (see ["Integrating C functions" on page 591](../C-Level_Extensibility/Integrating_C_functions.md)). Then create a JSFL file with the following code, and store it in the Configuration/Commands directory (see ["Saving JSFL files" on page 2](../Introduction/Working_with_the_JavaScript_API.md)).

```javascript
// JSFL file to run C function defined above. 
var a = 5;
var b = 10;
var sum = Sample.computeSum(a, b);
fl.trace("The sum of " + a + " and " + b + " is " + sum );
```

To run the function defined in the DLL, select Commands > Sample in the Flash authoring environment.

