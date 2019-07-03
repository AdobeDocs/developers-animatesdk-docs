## symbolInstance.colorRedAmount

#### Availability

Flash MX 2004.

#### Usage

symbolInstance.colorRedAmount

#### Description

Property; an integer that is part of the color transformation for the instance. This property is equivalent to using the Color \Advanced setting in the instance Property inspector. Allowable values are from -255 to 255.

#### Example

```
The following example sets the colorRedAmount of the selected symbol instance to 255:
fl.getDocumentDOM().selection\[0\].colorRedAmount = 255;

```