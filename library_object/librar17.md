## library.setItemProperty()

#### Availability

Flash MX 2004.

#### Usage

library.setItemProperty(property, value)

#### Parameters

**property** A string that is the name of the property to set. For a list of properties, see the Property summary table for the [Item object](#_bookmark658) and property summaries for its subclasses. To see which objects are subclasses of the Item object, see ["Summary of the DOM structure" on page 14](#_bookmark7).
**value** The value to assign to the specified property.

#### Returns

Nothing.

#### Description

Method; sets the property for all selected library items (ignoring folders).

#### Example

```
The following example assigns the value button to the symbolType property for the selected library item or items. In this case, the item must be a [SymbolItem object](#_bookmark950); symbolType is a valid property for SymbolItem objects.
fl.getDocumentDOM().library.setItemProperty("symbolType", "button");

```