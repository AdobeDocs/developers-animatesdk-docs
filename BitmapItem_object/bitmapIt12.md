## bitmapItem.useDeblocking

#### Availability

Flash CS4 Professional.

#### Usage

bitmapItem.useDeblocking

#### Description

Property; a Boolean value that specifies whether deblocking is enabled (true) or not (false).

#### Example

```
Assuming the first item in the Library is a bitmap item, the following code enables deblocking for the item:
var libItem = fl.getDocumentDOM().library.items\[0\]; libItem.useDeblocking = true;

```