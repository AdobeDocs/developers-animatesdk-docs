## symbolItem.sourceAutoUpdate

#### Availability

Flash MX 2004.

#### Usage

symbolItem.sourceAutoUpdate

#### Description

Property; a Boolean value that specifies whether the item is updated when the FLA file is published. The default value is false. Used for shared library symbols.

#### Example

```
The following example sets the sourceAutoUpdate property for a library item:
fl.getDocumentDOM().library.items\[0\].sourceAutoUpdate = true;

```