## textAttrs.target

#### Availability

Flash MX 2004.

#### Usage

*textAttrs.target*

#### Description

Property; a string that represents the target property of the text field. This property works only with static text.

#### Example

The following example gets the target property of the text field in the first frame of the top layer of the current scene and shows it in the Output panel:

```javascript
fl.outputPanel.trace(fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0].getTe xtAttr("target"));

```