## camera.colorFilterEnabled	

#### Availability

Animate 2019

#### Usage

camera.colorFilterEnabled	

#### Return

Boolean value true if color filter is enabled otherwise false.

#### Description

Property; Used to Enable/Disable camera's color Filter.

#### Example

The following example enables the color filter:

```javascript
var timeline = an.getDocumentDOM().getTimeline();

fl.trace(timeline.camera.colorFilterEnabled = true);

```