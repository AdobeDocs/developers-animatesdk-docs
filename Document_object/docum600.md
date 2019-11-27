## document.setPlayerVersion()

#### Availability

Flash CS3 Professional.

#### Usage

document.setPlayerVersion(version)

#### Parameters

**version** A string that represents the version of Flash Player targeted by the specified document. Acceptable values are "FlashLite", "FlashLite11", "FlashLite20" , "FlashLite30", "1", "2", "3", "4", "5", "6", "7", "8", "9", "FlashPlayer10", "FlashPlayer10.3", "FlashPlayer11.1", "FlashPlayer11.2", "FlashPlayer11.3","FlashPlayer11.4", "FlashPlayer11.5", "FlashPlayer11.6", "FlashPlayer11.7", "AdobeAIR1_1", "AdobeAIR1_1", "AdobeAIR2_5", "AdobeAIR3_6", "android3_6", and "PF13_6".

#### Returns

A value of true if the player version was successfully set; false otherwise.

#### Description

Method; sets the version of the Flash Player targeted by the specified document. This is the same value as that set in the Publish Settings dialog box.

#### Example

```javascript
The following example targets Flash Player 6 as the player version for the current document:
fl.getDocumentDOM().setPlayerVersion("6");

```
#### See also

[document.getPlayerVersion()](../Document_object/docume82.md)
