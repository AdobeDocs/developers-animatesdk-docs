## About extensibility

This chapter describes the C-level extensibility mechanism, which lets you implement Adobe Flash Professional extensibility files using a combination of JavaScript and custom C code.
***Note:** Adobe Animate runs on 64-bit operating systems only. All C extensions for this release must be built (or rebuilt) for 64 bit support.*
To implement extensibility, you define functions using C, bundle them in a dynamic linked library (DLL) or a shared library, save the library in the appropriate directory, and then call the functions from JavaScript using the Adobe Animate JavaScript API.
For example, you might want to define a function that performs intense calculations more efficiently than JavaScript does, which improves performance, or when you want to create more advanced tools or effects.
This extensibility mechanism is a subset of the Adobe Dreamweaver CS3 API. If you are familiar with that API, you might recognize the functions in the C-level extensibility mechanism API. However, this API differs from the Dreamweaver API in the following ways:

-   This API does not contain all the commands in the Dreamweaver API.

-   All declarations of type wchar\_t and char in the Dreamweaver API are implemented as unsigned short

declarations in this API, to support Unicode when strings are passed.

-   The [JSVal JS\_BytesToValue()](#_bookmark1180) function in this API is not part of the Dreamweaver API.

-   The location in which the DLL or shared library files must be stored is different (see ["Integrating C functions" on page 591](#Integrating_C_functions)).

<span id="Integrating_C_functions" class="anchor"></span>

