## symbolInstance.colorRedPercent

#### Availability

Flash MX 2004.

#### Usage

symbolInstance.colorRedPercent

#### Description

Property; part of the color transformation for the instance. This property is equivalent to using the Color >Advanced setting in the instance Property inspector (the percentage controls on the left of the dialog box). This value sets the red values to a specified percentage. Allowable values are from -100 to 100.

#### Example

The following example sets the colorRedPercent of the selected symbol instance to 10:
```javascript
fl.getDocumentDOM().selection[0].colorRedPercent = 10;

```