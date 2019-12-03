## symbolInstance.firstFrame

#### Availability

Flash MX 2004.

#### Usage

symbolInstance.firstFrame

#### Description

Property; a zero-based integer that specifies the first frame to appear in the timeline of the graphic. This property applies only to graphic symbols and sets the same property as the First field in the Property inspector. For other types of symbols, this property is undefined.

#### Example

The following example specifies that Frame 10 should be the first frame to appear in the timeline of the specified element:

```javascript
fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0].firstFrame = 10;

```