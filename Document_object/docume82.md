## document.getPlayerVersion()

#### Availability

Flash CS3 Professional.

#### Usage

document.getPlayerVersion()

#### Parameters

None.

#### Returns

A string that represents the Flash Player version specified by using document.setPlayerVersion(). If no value has been set, returns the value specified in the Publish Settings dialog box.

#### Description

Method; returns a string that represents the targeted player version for the specified document. For a list of values that this method can return, see [document.setPlayerVersion()](#_bookmark299).
To determine which version of ActionScript is being targeted in the specified file, use [document.asVersion](#_bookmark140).

#### Example

```
The following example illustrates targeting specified player versions for the current document and then retrieving those values:
fl.getDocumentDOM().setPlayerVersion("6");
var version = fl.getDocumentDOM().getPlayerVersion(); fl.trace(version) // displays "6" fl.getDocumentDOM().setPlayerVersion("FlashPlayer10"); var version = fl.getDocumentDOM().getPlayerVersion(); fl.trace(version) // displays ""FlashPlayer10""

```
#### See also

[document.setPlayerVersion()](#_bookmark299)
