## document.setPlayerVersion()

#### Availability

> Flash CS3 Professional.

#### Usage

> document.setPlayerVersion(version)

#### Parameters

> **version** A string that represents the version of Flash Player targeted by the specified document. Acceptable values are "FlashLite", "FlashLite11", "FlashLite20" , "FlashLite30", "1", "2", "3", "4", "5", "6", "7", "8", "9", "FlashPlayer10", "FlashPlayer10.3", "FlashPlayer11.1", "FlashPlayer11.2", "FlashPlayer11.3","FlashPlayer11.4", "FlashPlayer11.5", "FlashPlayer11.6", "FlashPlayer11.7", "AdobeAIR1\_1", "AdobeAIR1\_1", "AdobeAIR2\_5", "AdobeAIR3\_6", "android3\_6", and "PF13\_6".

#### Returns

> A value of true if the player version was successfully set; false otherwise.

#### Description

> Method; sets the version of the Flash Player targeted by the specified document. This is the same value as that set in the Publish Settings dialog box.

#### Example

> The following example targets Flash Player 6 as the player version for the current document:
>
> fl.getDocumentDOM().setPlayerVersion("6");

#### See also

> [document.getPlayerVersion()](#_bookmark211)
