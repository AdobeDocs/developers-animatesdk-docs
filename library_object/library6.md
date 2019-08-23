## library.getItemProperty()

#### Availability

Flash MX 2004.

#### Usage

library.getItemProperty(property)

#### Parameters

**property** A string. For a list of values that you can use as a *property* parameter, see the Property summary table for the [Item object](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item_summary.md), along with property summaries for its subclasses.

#### Returns

A string value for the property.

#### Description

Method; gets the property for the selected item.

#### Example

```javascript
The following example shows a dialog box that contains the Linkage Identifier value for the symbol when referencing it using ActionScript or for run-time sharing:
alert(fl.getDocumentDOM().library.getItemProperty("linkageIdentifier"));

```