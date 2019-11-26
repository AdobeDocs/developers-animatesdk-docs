## document.getMobileSettings()

#### Availability

Flash CS3 Professional.

#### Usage

document.getMobileSettings()

#### Parameters

None.

#### Returns

A string that represents the XML settings for the document. If no value has been set, returns an empty string.

#### Description

Method; returns the mobile XML settings for the document.

#### Example

```javascript
The following example displays the XML settings string for the current document:
fl.trace(fl.getDocumentDOM().getMobileSettings());
//traces a string like the following
"<? xml version="1.0" encoding="UTF-16" standalone="no"
?><mobileSettings><contentType id="standalonePlayer" name="Standalone Player"/><testDevices><testDevice id="1170" name="Generic Phone" selected="yes"/></testDevices><outputMsgFiltering info="no" trace="yes" warning="yes"/><testWindowState height="496" splitterClosed="No" splitterXPos="400" width="907"/></mobileSettings>"

```
#### See also

[document.setMobileSettings()](../Document_object/docum580.md)
