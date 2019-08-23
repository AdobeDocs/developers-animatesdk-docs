## timeline.getGuidelines()

#### Availability

Flash CS4 Professional.

#### Usage

timeline.getGuidelines()

#### Parameters

None.

#### Returns

An XML string.

#### Description

Method: returns an XML string that represents the current positions of the horizontal and vertical guide lines for a timeline (View \Guides \>Show Guides). To apply these guide lines to a timeline, use [timeline.setGuidelines()](#!AdobeDocs/developers-animatesdk-docs/master/Timeline_object/timeli44.md).

#### Example

```javascript
Assuming that you have some guide lines on the first timeline, the following example displays them as an XML string in the Output panel:
var currentTimeline = fl.getDocumentDOM().timelines\[0\]; fl.trace(currentTimeline.getGuidelines());

```