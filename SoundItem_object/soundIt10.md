## soundItem.sourceFileExists

#### Availability

> Flash CS4 Professional.

#### Usage

> soundItem.sourceFileExists

#### Description

> Read-only property: a Boolean value of true if the file that was imported to the Library still exists in the location from where it was imported; false otherwise.

#### Example

> Assuming that the first item in the Library is a sound item, the following code displays "true" if the file that was imported into the Library still exists.
>
> var libItem = fl.getDocumentDOM().library.items\[0\]; fl.trace("sourceFileExists = "+ libItem.sourceFileExists);

#### See also

> [soundItem.sourceFileIsCurrent](#soundItem.sourceFileIsCurrent), [soundItem.sourceFilePath](#_bookmark841)

<span id="soundItem.sourceFileIsCurrent" class="anchor"></span>
