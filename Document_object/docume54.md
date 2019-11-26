## document.duplicatePublishProfile()

#### Availability

Flash MX 2004.

#### Usage

document.duplicatePublishProfile([profileName])

#### Parameters

**profileName** A string that specifies the unique name of the duplicated profile. If you do not specify a name, the method uses the default name. This parameter is optional.

#### Returns

An integer that is the index of the new profile in the profile list. Returns -1 if the profile cannot be duplicated.

#### Description

Method; duplicates the currently active profile and gives the duplicate version focus.

#### Example

```javascript
The following example duplicates the currently active profile and displays the index of the new profile in the Output panel:
fl.trace(fl.getDocumentDOM().duplicatePublishProfile("dup profile"));

```