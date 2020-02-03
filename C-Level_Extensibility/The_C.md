## The C-level API

The C-level extensibility API consists of the JSBool (*JSNative) function signature and the following functions:

-   [JSBool JS\_DefineFunction()](#jsbool-js_definefunction)

-   [unsigned short \*JS\_ValueToString()](#unsigned-short-js_valuetostring)

-   [JSBool JS\_ValueToInteger()](#jsbool-js_valuetointeger)

-   [JSBool JS\_ValueToDouble()](#jsbool-js_valuetodouble)

-   [JSBool JS\_ValueToBoolean()](#jsbool-js_valuetoboolean)

-   [JSBool JS\_ValueToObject()](#jsbool-js_valuetoobject)

-   [JSBool JS\_StringToValue()](#jsbool-js_stringtovalue)

-   [JSBool JS\_DoubleToValue()](#jsbool-js_doubletovalue)

-   [JSVal JS\_BooleanToValue()](#jsval-js_booleantovalue)

-   [JSVal JS\_BytesToValue()](#jsval-js_bytestovalue)

-   [JSVal JS\_IntegerToValue()](#jsval-js_integertovalue)

-   [JSVal JS\_ObjectToValue()](#jsval-js_objecttovalue)

-   [unsigned short \*JS\_ObjectType()](#unsigned-short-js_objecttype)

-   [JSObject \*JS\_NewArrayObject()](#jsobject-js_newarrayobject)

-   [long JS\_GetArrayLength()](#long-js_getarraylength)

-   [JSBool JS\_GetElement()](#jsbool-js_getelement)

-   [JSBool JS\_SetElement()](#jsbool-js_setelement)

-   [JSBool JS\_ExecuteScript()](#jsbool-js_executescript)

***Note:** Adobe Animate runs on 64-bit operating systems only. All C extensions for this release must be built (or rebuilt) for 64 bit support.*

### typedef JSBool (*JSNative)(JSContext *cx, JSObject *obj, unsigned int argc, jsval *argv, jsval *rval)

#### Description

Method; describes C-level implementations of JavaScript functions in the following situations:

-   The *cx* pointer is a pointer to an opaque JSContext structure, which must be passed to some of the functions in the JavaScript API. This variable holds the interpreter’s execution context.

-   The *obj* pointer is a pointer to the object in whose context the script executes. While the script is running, the this

keyword is equal to this object.

-   The *argc* integer is the number of arguments being passed to the function.

-   The *argv* pointer is a pointer to an array of jsval structures. The array is argc elements in length.

-   The *rval* pointer is a pointer to a single jsval structure. The function’s return value should be written to *rval.

The function returns JS_TRUE if successful; JS_FALSE otherwise. If the function returns JS_FALSE, the current script stops executing and an error message appears.

### JSBool JS_DefineFunction()

#### Usage

*JSBool JS_DefineFunction(unsigned short *name, JSNative call, unsigned int nargs)*

#### Description

Method; registers a C-level function with the JavaScript interpreter in Animate. After the JS\_DefineFunction() function registers the C-level function that you specify in the *call* argument, you can invoke it in a JavaScript script by referring to it with the name that you specify in the *name* argument. The *name* argument is case-sensitive.

Typically, this function is called from the MM_Init() function, which Animate calls during startup.

#### Arguments

unsigned short **name*, JSNative*call*, unsigned int *nargs*

-   The *name* argument is the name of the function as it is exposed to JavaScript.

-   The *call* argument is a pointer to a C-level function. The function must return a JSBool, which indicates success or failure.

-   The *nargs* argument is the number of arguments that the function expects to receive.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

### unsigned short *JS_ValueToString()

#### Usage

*unsigned short *JS_ValueToString(JSContext *cx, jsval v, unsigned int *pLength)*

#### Description

Method; extracts a function argument from a jsval structure, converts it to a string, if possible, and passes the converted value back to the caller.

***Note:** Do not modify the returned buffer pointer or you might corrupt the data structures of the JavaScript interpreter. To change the string, you must copy the characters into another buffer and create a new JavaScript string.*

#### Arguments

JSContext **cx*, jsval *v*, unsigned int **pLength*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *v* argument is the jsval structure from which the string is to be extracted.

-   The *pLength* argument is a pointer to an unsigned integer. This function sets *plength equal to the length of the string in bytes.

#### Returns

A pointer that points to a null-terminated string if successful or to a null value on failure. The calling routine must not free this string when it finishes.

### JSBool JS\_ValueToInteger()

#### Usage

JSBool JS\_ValueToInteger(JSContext \*cx, jsval v, long \*lp);

#### Description

Method; extracts a function argument from a jsval structure, converts it to an integer (if possible), and passes the converted value back to the caller.

#### Arguments

JSContext **cx*, jsval *v*, long **lp*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *v* argument is the jsval structure from which the integer is to be extracted.

-   The *lp* argument is a pointer to a 4-byte integer. This function stores the converted value in *lp.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

### JSBool JS_ValueToDouble()

#### Usage

JSBool JS_ValueToDouble(JSContext *cx, jsval v, double *dp);

#### Description

Method; extracts a function argument from a jsval structure, converts it to a double (if possible), and passes the converted value back to the caller.

#### Arguments

JSContext **cx*, jsval *v*, double **dp*

-   The *cx* argument is the opaque JSContext pointer that passed to the JavaScript function.

-   The *v* argument is the jsval structure from which the double is to be extracted.

-   The *dp* argument is a pointer to an 8-byte double. This function stores the converted value in *dp.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

### JSBool JS_ValueToBoolean()

#### Usage

JSBool JS_ValueToBoolean(JSContext *cx, jsval v, JSBool *bp);

#### Description

Method; extracts a function argument from a jsval structure, converts it to a Boolean value (if possible), and passes the converted value back to the caller.

#### Arguments

JSContext **cx*, jsval *v*, JSBool **bp*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *v* argument is the jsval structure from which the Boolean value is to be extracted.

-   The *bp* argument is a pointer to a JSBool Boolean value. This function stores the converted value in *bp.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

### JSBool JS_ValueToObject()

#### Usage

*JSBool JS_ValueToObject(JSContext *cx, jsval v, JSObject **op);*

#### Description

Method; extracts a function argument from a jsval structure, converts it to an object (if possible), and passes the converted value back to the caller. If the object is an array, use *JS_GetArrayLength()* and *JS_GetElement()* to read its contents.

#### Arguments

JSContext **cx*, jsval *v*, JSObject ***op*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *v* argument is the jsval structure from which the object is to be extracted.

-   The *op* argument is a pointer to a JSObject pointer. This function stores the converted value in *op.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

### JSBool JS\_StringToValue()

#### Usage

*JSBool JS_StringToValue(JSContext *cx, unsigned short *bytes, uint sz, jsval *vp);*

#### Description

Method; stores a string return value in a jsval structure. It allocates a new JavaScript string object.

#### Arguments

JSContext **cx*, unsigned short **bytes*, size_t*sz*, jsval **vp*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *bytes* argument is the string to be stored in the jsval structure. The string data is copied, so the caller should free the string when it is not needed. If the string size is not specified (see the *sz* argument), the string must be null-terminated.

-   The *sz* argument is the size of the string, in bytes. If *sz* is 0, the length of the null-terminated string is computed automatically.

-   The *vp* argument is a pointer to the jsval structure into which the contents of the string should be copied.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

### JSBool JS\_DoubleToValue()

#### Usage

*JSBool JS_DoubleToValue(JSContext *cx, double dv, jsval *vp);*

#### Description

Method; stores a floating-point number return value in a jsval structure.

#### Arguments

JSContext **cx*, double *dv*, jsval **vp*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *dv* argument is an 8-byte floating-point number.

-   The *vp* argument is a pointer to the jsval structure into which the contents of the double should be copied.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

### JSVal JS_BooleanToValue()

#### Usage

*jsval JS_BooleanToValue(JSBool bv);*

#### Description

Method; stores a Boolean return value in a jsval structure.

#### Arguments

JSBool *bv*

-   The *bv* argument is a Boolean value: *JS_TRUE* indicates success; *JS_FALSE* indicates failure.

#### Returns

A JSVal structure that contains the Boolean value that passes to the function as an argument.

### JSVal JS_BytesToValue()

#### Usage

*JSBool JS_BytesToValue(JSContext *cx, unsigned short *bytes, uint sz, jsval *vp);*

#### Description

Method; converts bytes to a JavaScript value.

#### Arguments

JSContext **cx*, unsignedshort\*bytes, uint*sz*, jsval **vp*

-   The *cx* argument is the JavaScript context.

-   The *bytes* argument is the string of bytes to convert to a JavaScript object.

-   The *sz* argument is the number of bytes to be converted.

-   The *vp* argument is the JavaScript value.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

### JSVal JS_IntegerToValue()

#### Usage

*jsval JS_IntegerToValue(long lv);*

#### Description

Method; converts a long integer value to JSVal structure.

#### Arguments

*lv*
The *lv* argument is the long integer value that you want to convert to a jsval structure.

#### Returns

A JSVal structure that contains the integer that passed to the function as an argument.

### JSVal JS_ObjectToValue()

#### Usage

*jsval JS_ObjectToValue(JSObject \*obj);*

#### Description

Method; stores an object return value in a JSVal. Use *JS_NewArrayObject()* to create an array object; use *JS_SetElement()* to define its contents.

#### Arguments

JSObject **obj*
The *obj* argument is a pointer to the JSObject object that you want to convert to a JSVal structure.

#### Returns

A JSVal structure that contains the object that you passed to the function as an argument.

### unsigned short \*JS\_ObjectType()

#### Usage

*unsigned short \*JS_ObjectType(JSObject \*obj);*

#### Description

Method; given an object reference, returns the class name of the object. For example, if the object is a DOM object, the function returns "Document". If the object is a node in the document, the function returns "Element". For an array object, the function returns "Array".

***Note:** Do not modify the returned buffer pointer, or you might corrupt the data structures of the JavaScript interpreter.*

#### Arguments

JSObject **obj*
Typically, this argument is passed in and converted using the JS_ValueToObject() function.

#### Returns

A pointer to a null-terminated string. The caller should not free this string when it finishes.

### JSObject *JS_NewArrayObject()

#### Usage

*JSObject \*JS\_NewArrayObject(JSContext \*cx, unsigned int length \[, jsval \*v\])*

#### Description

Method; creates a new object that contains an array of JSVals.

#### Arguments

JSContext **cx*, unsigned int *length*, jsval **v*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *length* argument is the number of elements that the array can hold.

-   The *v* argument is an optional pointer to the jsvals to be stored in the array. If the return value is not null, *v* is an array that contains *length* elements. If the return value is null, the initial content of the array object is undefined and can be set using the *JS_SetElement()* function.

#### Returns

A pointer to a new array object or the value null upon failure.

### long JS_GetArrayLength()

#### Usage

*long JS_GetArrayLength(JSContext \*cx, JSObject \*obj)*

#### Description

Method; given a pointer to an array object, gets the number of elements in the array.

#### Arguments

JSContext **cx*, JSObject*\*obj*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *obj* argument is a pointer to an array object.

#### Returns

The number of elements in the array or -1 upon failure.

### JSBool JS_GetElement()

#### Usage

*JSBool JS_GetElement(JSContext \*cx, JSObject \*obj, jsint idx, jsval \*vp)*

#### Description

Method; reads a single element of an array object.

#### Arguments

JSContext **cx*, JSObject **obj*, jsint *idx*, jsval **vp*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *obj* argument is a pointer to an array object.

-   The *idx* argument is an integer index into the array. The first element is index 0, and the last element is index (length 1-).

-   The *vp* argument is a pointer to a jsval where the contents of the jsval structure in the array should be copied.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

### JSBool JS_SetElement()

#### Usage

*JSBool JS_SetElement(JSContext \*cx, JSObject \*obj, jsint idx, jsval \*vp)*

#### Description

Method; writes a single element of an array object.

#### Arguments

JSContext **cx*, JSObject **obj*, jsint *idx*, jsval **vp*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *obj* argument is a pointer to an array object.

-   The *idx* argument is an integer index into the array. The first element is index 0, and the last element is index (length 1-).

-   The *vp* argument is a pointer to a jsval structure whose contents should be copied to the jsval in the array.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

### JSBool JS_ExecuteScript()

#### Usage

*JS_ExecuteScript (JSContext \*cx, JSObject \*obj, unsigned short \*script, unsigned int sz, jsval
\*rval)*

#### Description

Method; compiles and executes a JavaScript string. If the script generates a return value, it returns in *rval.

#### Arguments

JSContext **cx*, JSObject **obj*, unsigned short **script*, unsigned int*sz*, jsval **rval*

-   The *cx* argument is the opaque JSContext pointer that passes to the JavaScript function.

-   The *obj* argument is a pointer to the object in whose context the script executes. While the script is running, the

this keyword is equal to this object. Usually this is the JSObject pointer that passes to the JavaScript function.

-   The *script* argument is a string that contains JavaScript code. If the string size is not specified (see the *sz* argument), the string must be null-terminated.

-   The *sz* argument is the size of the string. If *sz* is 0, the length of the null-terminated string is computed automatically.

-   The *rval* argument is a pointer to a single jsval structure. The function’s return value is stored in *rval.

#### Returns

A Boolean value: JS_TRUE indicates success; JS_FALSE indicates failure.

