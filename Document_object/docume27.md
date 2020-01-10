## document.canTestMovie()

#### Availability

Flash MX 2004.

#### Usage

document.canTestMovie()

#### Parameters

None.

#### Returns

A Boolean value: true if you can use the [document.testMovie()](../Document_object/docu5948.md) method successfully: false otherwise.

#### Description

Method; determines whether you can use the [document.testMovie()](../Document_object/docu5948.md) method successfully.

#### Example

```javascript
The following example tests whether fl.getDocumentDOM().testMovie() can be used. If so, it calls the method.

if(fl.getDocumentDOM().canTestMovie())
{ 
    fl.getDocumentDOM().testMovie();
}

```
#### See also

[document.canTestScene()](../Document_object/docume28.md), [document.testScene()](../Document_object/docu5979.md)

<span id="document.canTestScene()" class="anchor"></span>
