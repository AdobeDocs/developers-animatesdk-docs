## document.frameRate

#### Availability

Flash MX 2004.

#### Usage

document.frameRate

#### Description

Property; a float value that specifies the number of frames displayed per second when the SWF file plays; the default is 12. Setting this property is the same as setting the default frame rate in the Document Properties dialog box (Modify>
Document) in the FLA file.

#### Example

```javascript
The following example sets the frame rate to 25.5 frames per second:
fl.getDocumentDOM().frameRate = 25.5;

```