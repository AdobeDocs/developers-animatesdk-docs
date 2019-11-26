## fontItem.bitmap

#### Availability

Flash CS4 Professional.

#### Usage

fontItem.bitmap

#### Description

Property; a Boolean value that specifies whether the Font item is bitmapped (true) or not (false).

#### Example

```javascript
Assuming that the first item in the Library is a Font item, the following code displays true in the Output panel if it is bitmapped, false if it is not:
var theItem = fl.getDocumentDOM().library.items[0];
fl.trace("bitmap: "+ theItem.bitmap);

```