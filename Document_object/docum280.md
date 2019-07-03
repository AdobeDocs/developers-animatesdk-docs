## document.renamePublishProfile()

#### Availability

Flash MX 2004.

#### Usage

document.renamePublishProfile(\[profileNewName\])

#### Parameters

**profileNewName** An optional parameter that specifies the new name for the profile. The new name must be unique. If the name is not specified, a default name is provided.

#### Returns

A Boolean value: true if the name is changed successfully; false otherwise.

#### Description

Method; renames the current profile.

#### Example

```
The following example renames the current profile to a default name and displays it:
alert(fl.getDocumentDOM().renamePublishProfile());

```