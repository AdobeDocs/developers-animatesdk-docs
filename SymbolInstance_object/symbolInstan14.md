## symbolInstance.colorMode

#### Availability

Flash MX 2004.

#### Usage

symbolInstance.colorMode

#### Description

Property; a string that specifies the color mode as identified in the symbol Property inspector Color pop-up menu. Acceptable values are "none", "brightness", "tint", "alpha", and "advanced".

#### Example

The following example changes the colorMode property of the first element in the first frame of the first layer in the timeline to alpha:
```javascript
fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0].colorMode = "alpha";

```