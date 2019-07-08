## document.revert()

#### Availability

Flash MX 2004.

#### Usage

document.revert()

#### Parameters

None.

#### Returns

Nothing.

#### Description

Method; reverts the specified document to its previously saved version. This method is equivalent to selecting File \Revert.

#### Example

```javascript
The following example reverts the current document to the previously saved version:
fl.getDocumentDOM().revert();

```
#### See also

[document.canRevert()](#_bookmark145), [fl.revertDocument()](#_bookmark528)
