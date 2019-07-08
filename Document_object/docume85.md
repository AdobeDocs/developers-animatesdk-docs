## document.getSWFPathFromProfile()

#### Availability

Flash Professional CS6.

#### Usage

document.getSWFPathFromProfile()

#### Parameters

None.

#### Returns

The full path to the SWF file that is set in the current Publish profile.

#### Description

Method; gets the path to the SWF file that is set in the current Publish profile.

#### Example

```javascript
The following example displays the full path to the SWF file as defined in the Publish profile:
fl.trace("the current Publish Setting's SWF file path is: " + fl.getDocumentDOM().getSWFPathFromProfile());

```