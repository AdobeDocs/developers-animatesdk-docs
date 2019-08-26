## symbolInstance.colorAlphaAmount

#### Availability

Flash MX 2004.

#### Usage

symbolInstance.colorAlphaAmount

#### Description

Property; an integer that is part of the color transformation for the instance, specifying the Advanced Effect Alpha settings. This property is equivalent to using the Color \Advanced setting in the Property inspector and adjusting the controls on the right of the dialog box. This value either reduces or increases the tint and alpha values by a constant amount. This value is added to the current value. This property is most useful if used with [symbolInstance.colorAlphaPercent](#!AdobeDocs/developers-animatesdk-docs/test/SymbolInstance_object/symbolInstanc9.md). Allowable values are from -255 to 255.

#### Example

```javascript
The following example subtracts 100 from the alpha setting of the selected symbol instance:
fl.getDocumentDOM().selection\[0\].colorAlphaAmount = -100;

<span id="symbolInstance.colorAlphaPercent" class="anchor"></span
```