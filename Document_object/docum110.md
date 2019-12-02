## document.loadCuepointXML() - dropped

#### Availability

Flash Professional CS5. Dropped in Adobe Animate.

#### Usage

document.loadCuepointXML(String URI)

#### Parameters

**URI** String; the absolute path to the cue point XML file.

#### Description

Dropped in Adobe Animate.
Method; loads a cue point XML file. The format and DTD of the XML file is the same as the one imported and exported by the Cue Points Property inspector. The return value is the same as the string serialized in the Cue Point property of the object containing the instance of an FLVPlayback Component.

#### Example


The following example the cue points XML file located at C:\\testCuePoints.xml:
```javascript

var cuePoints = fl.getDocumentDOM().LoadCuepointXML("c:\\testCuePoints.xml");

```