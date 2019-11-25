## document.as3Dialect

#### Availability

Flash CS3 Professional.

#### Usage

document.as3Dialect

#### Description

Property; a string that describes the ActionScript 3.0 "dialect" being used in the specified document. The default value is "AS3". If you wish to allow prototype classes, as permitted in earlier ECMAScript specifications, set this value to "ES".

#### Example

```javascript
The following example specifies that the dialect being used in the current document is ECMAScript:
fl.getDocumentDOM().as3Dialect="ES";

```
#### See also

[document.asVersion](../Document_object/docume21.md)
