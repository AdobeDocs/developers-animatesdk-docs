## timeline.setGuidelines()

#### Availability

Flash CS4 Professional.

#### Usage

timeline.setGuidelines(xmlString)

#### Parameters

**xmlString** An XML string that contains information on the guidelines to apply.

#### Returns

A Boolean value of true if the guidelines are successfully applied; false otherwise.

#### Description

Method: replaces the guide lines for the timeline (View \Guides \Show Guides) with the information specified in
*xmlString*. To retrieve an XML string that can be passed to this method, use [timeline.getGuidelines()](../Timeline_object/timeli23.md). To view the newly set guide lines, you may have to hide them and then view them.

#### Example

```javascript
The following example applies the guide lines from one FLA file to another FLA file:
var doc0 = fl.documents\[0\];
var guides0 = doc0.timelines\[0\].getGuidelines(); var doc1 = fl.documents\[1\]; doc1.timelines\[0\].setGuidelines(guides0);

```