## document.asVersion

#### Availability

Flash CS3 Professional.

#### Usage

document.asVersion

#### Description

Property; an integer that specifies which version of ActionScript is being used in the specified document. Acceptable values are 1, 2, and 3.
To determine the targeted player version for the specified document, use [document.getPlayerVersion()](#_bookmark211); this method returns a string, so it can be used by Flash® Lite™ players.

#### Example

```javascript
The following example sets the version of ActionScript in the current document to ActionScript 2.0 if it is currently set as ActionScript 1.0.
if(fl.getDocumentDOM().asVersion == 1){
fl.getDocumentDOM().asVersion = 2;
}

```
#### See also

[document.as3Dialect](#_bookmark136), [document.getPlayerVersion()](#_bookmark211)
