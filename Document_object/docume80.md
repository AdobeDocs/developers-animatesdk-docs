## document.getMetadata()

#### Availability

Flash 8.

#### Usage

document.getMetadata()

#### Parameters

None.

#### Returns

A string containing the XML metadata associated with the document or an empty string if there is no metadata.

#### Description

Method; returns a string containing the XML metadata associated with the document, or an empty string if there is no metadata.

#### Example

```
The following example displays XML metadata from the current document in the Output panel:
fl.trace("XML Metadata is :" + fl.getDocumentDOM().getMetadata());

```
#### See also

[document.setMetadata()](#_bookmark295)
