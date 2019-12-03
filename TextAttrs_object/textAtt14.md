## textAttrs.rotation

#### Availability

Flash MX 2004.

#### Usage

*textAttrs.rotation*

#### Description

Property; a Boolean value. A value of true causes Flash to rotate the characters of the text 90º. The default value is *false*. This property applies only to static text with a vertical orientation; it generates a warning if used with other text types.

#### Example

The following example sets the rotation of the selected text field to true: 

```javascript
fl.getDocumentDOM().setElementTextAttr("rotation", true);

```