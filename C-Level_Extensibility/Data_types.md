## Data types

The JavaScript interpreter defines the data types described in this section.

### typedef struct JSContext JSContext

A pointer to this opaque data type passes to the C-level function. Some functions in the API accept this pointer as one of their arguments.

### typedef struct JSObject JSObject

A pointer to this opaque data type passes to the C-level function. This data type represents an object, which might be an array object or some other object type.

### typedef struct jsval jsval

An opaque data structure that can contain an integer, or a pointer to a float, string, or object. Some functions in the API can read the values of function arguments by reading the contents of a *jsval* structure, and some can be used to write the function’s return value by writing a *jsval* structure.

### typedef enum { JS\_FALSE = 0, JS\_TRUE = 1 } JSBool

A simple data type that stores a Boolean value.

