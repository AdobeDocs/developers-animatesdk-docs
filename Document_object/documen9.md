## document.addNewPublishProfile()

#### Availability

Flash MX 2004.

#### Usage

document.addNewPublishProfile([profileName])

#### Parameters

**profileName** The unique name of the new profile. If you do not specify a name, a default name is provided. This parameter is optional.

#### Returns

An integer that is the index of the new profile in the profiles list. Returns -1 if a new profile cannot be created.

#### Description

Method; adds a new publish profile and makes it the current one.

#### Example


The following example adds a new publish profile with a default name and then displays the name of the profile in the Output panel:
```javascript
fl.getDocumentDOM().addNewPublishProfile();
fl.outputPanel.trace(fl.getDocumentDOM().currentPublishProfile);
```
The following example adds a new publish profile with the name "my profile":  

```javascript
fl.getDocumentDOM().addNewPublishProfile("my profile");

```
#### See also

[document.deletePublishProfile()](../Document_object/docume42.md)
