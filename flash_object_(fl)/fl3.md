## fl.browseForFileURL()

#### Availability

Flash MX 2004.

#### Usage

fl.browseForFileURL(browseType [, title [, fileDescription [, fileFilter]]])

#### Parameters

**browseType** A string that specifies the type of file browse operation. Valid values are "open", "select" or "save". The values "open" and "select" open the system File Open dialog box. Each value is provided for compatibility with Dreamweaver. The value "save" opens a system File Save dialog box.

**title** An optional string that specifies the title for the File Open or File Save dialog box. If this parameter is omitted, a default value is used. This parameter is optional.

**fileDescription** An optional string that specifies a file description, for example:

FLA Document (*.fla)
ActionScript File (*.as)

**fileFilter** An optional string that specifies a filter, such that only files that match the filters are displayed in the dialog, for example:

"fla"
"fla;as"
"jsfl;fla;as"

#### Returns

The URL of the file, expressed as a file:/// URI; returns null if the user cancels out of the dialog box.

#### Description

Method; opens a File Open or File Save system dialog box and lets the user specify a file to be opened or saved.

#### Example

The following examples illustrate various options of the fl.browseForFileURL() method:
```javascript

//CC
var uri = fl.browseForFileURL("open", "Select a FLA", "FLA Document (*.fla)", "fla");
or
var fileDescription = "FLA document (*.fla);Actionscript File (*.as)";
var fileFilter = "fla;as";
var uri = fl.browseForFileURL("open", "Select a FLA or AS file", fileDescription, fileFilter);

//The following are for CS4 through CS6. They do not work in CC.
var fileURL = fl.browseForFileURL("open", "Select file");

var doc = fl.openDocument(fileURL);
// The macFormat and winFormat parameters are supported in Flash CS4 through CS6.
// To enable only FLA files in the open file dialog
var macFormat = "Flash Document|SPA||";
var winFormat = "Flash Document|*.fla||";
var previewArea = {};
var uri = fl.browseForFileURL("open", "Select a FLA file", previewArea, macFormat, winFormat);

// To enable only AS files in the open file dialog
var macFormat = "ActionScript File|TEXT[*.as||";
var winFormat = "ActionScript File|*.as||";
var previewArea = {};
var uri = fl.browseForFileURL("open", "Select a FLA file", previewArea, macFormat, winFormat);

// To enable only FLA and AS files in the open file dialog
var macFormat = "Flash Document|SPA[*.fla|ActionScript File|TEXT[*.as||";
var winFormat = "Flash Document|*.fla|ActionScript File|*.as||";
var previewArea = {};
var uri = fl.browseForFileURL("open", "Select a FLA or AS file", previewArea, macFormat,
winFormat);

```
#### See also

[fl.browseForFolderURL()](#fl.browseForFolderURL())

<span id="fl.browseForFolderURL()" class="anchor"></span>
