## symbolInstance.buttonTracking

#### Availability

Flash MX 2004.

#### Usage

symbolInstance.buttonTracking

#### Description

Property; a string that, for button symbols only, sets the same property as the pop-up menu for Track As Button or Track As Menu Item in the Property inspector. For other types of symbols, this property is ignored. Acceptable values are "button" or "menu".

#### Example

```
The following example sets the first symbol in the first frame of the first layer in the timeline to a Track As Menu Item, as long as that symbol is a button:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].buttonTracking = "menu";

```