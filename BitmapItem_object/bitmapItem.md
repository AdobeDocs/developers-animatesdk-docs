## bitmapItem.allowSmoothing

#### Availability

Flash MX 2004.

#### Usage

*bitmapItem.allowSmoothing*

#### Description

Property; a Boolean value that specifies whether to allow smoothing of a bitmap *(true)* or not *(false)*.

#### Example

```javascript
The following code sets the allowSmoothing property of the first item in the library of the current document to true:

fl.getDocumentDOM().library.items[0].allowSmoothing = true; 
alert(fl.getDocumentDOM().library.items[0].allowSmoothing);

```