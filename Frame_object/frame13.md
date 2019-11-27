## frame.isEmpty()

#### Availability

Adobe Animate.

#### Usage

*frame.isEmpty()*

#### Description

Method; a Boolean value. Lets you know whether the frame contains any elements.

#### Example

```javascript
The following example illustrates use of this method.

var frame = fl.getDocumentDOM().getTimeline().layers[0].frames[0]; 
if (frame.isEmpty) fl.trace("first frame is empty");

```