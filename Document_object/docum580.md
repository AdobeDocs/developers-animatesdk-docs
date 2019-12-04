## document.setMobileSettings()

#### Availability

Flash CS3 Professional.

#### Usage

document.setMobileSettings(xmlString)

#### Parameters

**xmlString** A string that describes the XML settings in a mobile FLA file.

#### Returns

A value of true if the settings were successfully set; false otherwise.

#### Description

Method; sets the value of an XML settings string in a mobile FLA file. (Most mobile FLA files have an XML string that describes the settings within the document.)

#### Example

The following example sets the XML settings string for a mobile FLA file. Note that the example below represents a single line of code.

```javascript

fl.getDocumentDOM().setMobileSettings("<? xml version="1.0" encoding="UTF-16" standalone="no"
?><mobileSettings><contentType id="standalonePlayer" name="Standalone Player"/><testDevices><testDevice id="1170" name="Generic Phone" selected="yes"/></testDevices><outputMsgFiltering info="no" trace="yes" warning="yes"/><testWindowState height="496" splitterClosed="No" splitterXPos="400" width="907"/></mobileSettings>");

```
#### See also

[document.getMobileSettings()](../Document_object/docume81.md)
