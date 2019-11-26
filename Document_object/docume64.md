## document.exportPNG()

#### Availability

Flash 8.

#### Usage

document.exportPNG([fileURI [, bCurrentPNGSettings [, bCurrentFrame]]])

#### Parameters

**fileURI** A string, expressed as a file:/// URI, that specifies the filename for the exported file. If *fileURI* is an empty string or is not specified, Flash displays the Export Movie dialog box.
**bCurrentPNGSettings** A Boolean value that specifies whether to use the current PNG publish settings (true) or to display the Export PNG dialog box (false). This parameter is optional. The default value is false.
**bCurrentFrame** A Boolean value that specifies whether to export only the current frame (true) or to export all frames, with each frame as a separate PNG file (false). This parameter is optional. The default value is false.

#### Returns

A Boolean value of true if the file is successfully exported as a PNG file; false otherwise.

#### Description

Method; exports the document as one or more PNG files. If *fileURI* is specified and the file already exists, it is overwritten without warning.
***Note:** If fileURI is empty and bCurrentFrame is true , the Export Movie dialog box does not display and Flash saves the exported PNG file in the same location as the .fla file.*
***Note:** If bCurrentPNGSettings is false and bCurrentFrame is true, the Export PNG dialog box does not display and Flash uses the current PNG publish settings.*

#### Example

```javascript
The following example exports the current frame in the current document to myFile.png, using the current PNG publish settings:
fl.getDocumentDOM().exportPNG("file:///C\|/myProject/myFile.png", true, true);

```