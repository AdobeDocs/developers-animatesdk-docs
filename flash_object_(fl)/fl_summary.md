## fl summary

#### Availability

Flash MX 2004.

#### Description

The flash object represents the Flash application. You can use flash or fl to refer to this object. This documentation uses fl in code samples throughout.

#### Method summary

The following methods can be used with the flash object:

| **Method**                                       | **Description**                                                                                                |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [fl.addEventListener()](#_bookmark451)           | Registers a function to be called when a specific event is received.                                           |
| [fl.browseForFileURL()](#_bookmark453)           | Opens a File Open or File Save system dialog box and lets the user specify a file to be opened or saved.       |
| [fl.browseForFolderURL()](#_bookmark455)         | Displays a Browse for Folder dialog box and lets the user select a folder.                                     |
| [fl.clearPublishCache()](#_bookmark456)          | Clears the publish cache.                                                                                      |
| [fl.clipCopyString()](#_bookmark457)             | Copies the specified string to the Clipboard.                                                                  |
| [fl.closeAll()](#_bookmark459)                   | Closes all open documents, displaying the Save As dialog box for any documents that were not previously saved. |
| [fl.closeAllPlayerDocuments()](#_bookmark460)    | Closes all the SWF files that were opened with Control \Test Movie.                                          |
| [fl.closeDocument()](#_bookmark461)              | Closes the specified document.                                                                                 |
| [fl.copyLibraryItem()](#_bookmark470)            | Silently copies a library item from a document without exposing the item in the Flash Pro user interface.      |
| [fl.createDocument()](#_bookmark471)             | Opens a new document and selects it.                                                                           |
| [fl.exportPublishProfileString()](#_bookmark478) | Uniform Resource Identifier (URI) from which to export publish settings.                                       |
| [fl.fileExists()](#_bookmark481)                 | Checks whether a file already exists on disk.                                                                  |
| [fl.findDocumentDOM()](#_bookmark482)            | Lets you target a specific file by using its unique identifier.                                                |
| [fl.findDocumentIndex()](#_bookmark484)          | Returns an array of integers that represent the position of a document in the fl.documents array.              |
| [fl.findObjectInDocByName()](#_bookmark486)      | Exposes elements with instance names that match specified text.                                                |
| [fl.findObjectInDocByType()](#_bookmark487)      | Exposes elements of a specified element type in a document.                                                    |
| [fl.getAppMemoryInfo()](#_bookmark489)           | Returns an integer that represents the number of bytes being used in a specified area of Flash.exe memory.     |
| [fl.getDocumentDOM()](#_bookmark490)             | Retrieves the DOM ([Document object](#_bookmark116)) of the currently active document.                         |

<table><thead><tr class="header"><th><strong>Method</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="#_bookmark495">fl.getSwfPanel()</a></td><td>Returns the SWFPanel object based on the panel's localized name or its SWF filename.</td></tr><tr class="even"><td><a href="#_bookmark492">fl.getThemeColor()</a></td><td>Retrieves a theme color that matches the parameter specified theme parameter name.</td></tr><tr class="odd"><td><a href="#_bookmark493">fl.getThemeColorParameters()</a></td><td>Retrieves an array of theme parameter names.</td></tr><tr class="even"><td><a href="#_bookmark494">fl.getThemeFontInfo()</a></td><td>Return either the font style or the font size that is used to draw the UI of the specified size.</td></tr><tr class="odd"><td><a href="#_bookmark497">fl.isFontInstalled()</a></td><td>Determines whether a specified font is installed.</td></tr><tr class="even"><td><a href="#_bookmark502">fl.mapPlayerURL()</a></td><td>Maps an escaped Unicode URL to a UTF-8 or MBCS URL.</td></tr><tr class="odd"><td><a href="#_bookmark508">fl.openDocument()</a></td><td>Opens a Flash (FLA) document for editing in a new Flash Document window and gives it focus.</td></tr><tr class="even"><td><a href="#_bookmark509">fl.openScript()</a></td><td>Opens a script (JSFL, AS, ASC) or other file (XML, TXT) in the Flash text editor.</td></tr><tr class="odd"><td><a href="#_bookmark520">fl.quit()</a></td><td>Quits Flash, prompting the user to save any changed documents.</td></tr><tr class="even"><td><a href="#_bookmark521">fl.reloadEffects() - dropped</a></td><td>Dropped in Adobe Animate.</td></tr><tr class="odd"><td><a href="#_bookmark522">fl.reloadTools()</a></td><td>Rebuilds the Tools panel from the toolconfig.xml file.</td></tr><tr class="even"><td><a href="#_bookmark524">fl.removeEventListener()</a></td><td><p>Unregisters a function that was registered using</p><p>fl.addEventListener().</p></td></tr><tr class="odd"><td><a href="#_bookmark525">fl.resetAS3PackagePaths()</a></td><td>Resets the global Classpath setting in the ActionScript 3.0 Settings dialog box to the default value.</td></tr><tr class="even"><td><a href="#_bookmark526">fl.resetPackagePaths() - dropped</a></td><td>Dropped in Adobe Animate.</td></tr><tr class="odd"><td><a href="#_bookmark529">fl.runScript()</a></td><td>Executes a JavaScript file.</td></tr><tr class="even"><td><a href="#_bookmark531">fl.saveAll()</a></td><td>Saves all open documents, displaying the Save As dialog box for any documents that were not previously saved.</td></tr><tr class="odd"><td><a href="#_bookmark533">fl.saveDocument()</a></td><td>Saves the specified document as a FLA document.</td></tr><tr class="even"><td><a href="#_bookmark535">fl.saveDocumentAs()</a></td><td>Displays the Save As dialog box for the specified document.</td></tr><tr class="odd"><td><a href="#_bookmark538">fl.selectElement()</a></td><td>Enables selection or editing of an element.</td></tr><tr class="even"><td><a href="#_bookmark539">fl.selectTool()</a></td><td>Selects the specified tool in the Tools panel.</td></tr><tr class="odd"><td><a href="#_bookmark540">fl.setActiveWindow()</a></td><td>Sets the active window to be the specified document.</td></tr><tr class="even"><td><a href="#_bookmark542">fl.setPrefBoolean()</a></td><td>Sets a boolean preference value.</td></tr><tr class="odd"><td><a href="#_bookmark541">fl.showIdleMessage()</a></td><td>Lets you disable the warning about a script running too long.</td></tr><tr class="even"><td><a href="#_bookmark548">fl.toggleBreakpoint()</a></td><td>Toggles a breakpoint for the given .as file at the given line.</td></tr><tr class="odd"><td><a href="#_bookmark551">fl.trace()</a></td><td>Sends a text string to the Output panel.</td></tr><tr class="even"><td><a href="#_bookmark554">fl.xmlPanel()</a></td><td>Launches the XML To UI dialog from a URI that points to an XML-format file.</td></tr><tr class="odd"><td><a href="#_bookmark555">fl.xmlPanelFromString()</a></td><td>Launches the XML To UI dialog from an XML-format string.</td></tr></tbody></table>

#### Property summary

The following properties can be used with the flash object.

| **Property**                                                           | **Description**                                                                                                                                                          |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [fl.actionsPanel](#fl.actionsPanel)                                    | Read-only; an [actionsPanel object](#_bookmark31).                                                                                                                       |
| [fl.as3PackagePaths](#_bookmark452)                                    | A string that corresponds to the global Classpath setting in the ActionScript 3.0 Settings dialog box.                                                                   |
| [fl.compilerErrors](#_bookmark462)                                     | Read-only; a [compilerErrors object](#_bookmark95).                                                                                                                      |
| [fl.componentsPanel](#_bookmark463)                                    | Read-only; a [componentsPanel object](#_bookmark104), which represents the Components panel.                                                                             |
| [fl.configDirectory](#_bookmark464)                                    | Read-only; a string that specifies the full path for the local user’s Configuration folder as a platform-specific path.                                                  |
| [fl.configURI](#_bookmark466)                                          | Read-only; a string that specifies the full path for the local user’s Configuration directory as a file:/// URI.                                                         |
| [fl.contactSensitiveSelection](#_bookmark468)                          | A Boolean value that specifies whether Contact Sensitive selection mode is enabled.                                                                                      |
| [fl.createNewDocList](#_bookmark472)                                   | Read-only; an array of strings that represent the various types of documents that can be created.                                                                        |
| [fl.createNewDocListType](#_bookmark473)                               | Read-only; an array of strings that represent the file extensions of the types of documents that can be created.                                                         |
| [fl.createNewTemplateList](#_bookmark474)                              | Read-only; an array of strings that represent the various types of templates that can be created.                                                                        |
| [fl.documents](#_bookmark475)                                          | Read-only; an array of Document objects (see [Document object](#_bookmark116)) that represent the documents (FLA files) that are currently open for editing.             |
| [fl.drawingLayer](#_bookmark477)                                       | The drawingLayer object that an extensible tool should use when the user wants to temporarily draw while dragging.                                                       |
| [fl.externalLibraryPath](#_bookmark479)                                | A string that contains a list of items in the global ActionScript 3.0 External library path, which specifies the location of SWC files used as runtime shared libraries. |
| [fl.flexSDKPath](#_bookmark488)                                        | A string that specifies the path to the Flex SDK folder, which contains bin, frameworks, lib, and other folders.                                                         |
| [fl.installedPlayers](#_bookmark496)                                   | Returns an array of generic objects corresponding to the list of installed Flash Players in the document Property inspector.                                             |
| [fl.languageCode](#_bookmark499)                                       | Returns the five character code identifying the locale of the application’s user interface.                                                                              |
| [fl.libraryPath](#_bookmark500)                                        | A string that contains a list of items in the global ActionScript 3.0 Library path, which specifies the location of SWC files or folders containing SWC files.           |
| [fl.Math](#_bookmark503)                                               | Read-only; the [Math object](#_bookmark718), which provides methods for matrix and point operations.                                                                     |
| [fl.mruRecentFileList](#_bookmark505)                                  | Read-only; an array of the complete filenames in the Most Recently Used (MRU) list that the Flash authoring tool manages.                                                |
| [fl.mruRecentFileListType](#_bookmark506)                              | Read-only; an array of the file types in the MRU list that the Flash authoring tool manages.                                                                             |
| [fl.packagePaths - dropped](#_bookmark512)                             | Dropped in Adobe Animate.                                                                                                                                                |
| [fl.publishCacheDiskSizeMax](#_bookmark515)                            | An integer that sets the disk cache size limit preference.                                                                                                               |
| [fl.publishCacheEnabled](#_bookmark516)                                | A boolean value that sets whether publish cache is enabled.                                                                                                              |
| [fl.publishCacheMemoryEntrySizeLim](#_bookmark517) [it](#_bookmark517) | An integer property that sets the maximum size for the memory cache entry preference.                                                                                    |

| **Property**                                  | **Description**                                                                                                                              |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [fl.publishCacheMemorySizeMax](#_bookmark518) | An integer that sets the memory cache size limit preference.                                                                                 |
| [fl.objectDrawingMode](#_bookmark507)         | An integer that represents the object drawing mode that is enabled.                                                                          |
| [fl.outputPanel](#_bookmark510)               | Read-only; reference to the [outputPanel object](#_bookmark734).                                                                             |
| [fl.presetPanel](#_bookmark513)               | Read-only; a [presetPanel object](#_bookmark779).                                                                                            |
| [fl.scriptURI](#_bookmark537)                 | Read-only; a string that represents the path of the currently running JSFL script, expressed as a file:/// URI.                              |
| [fl.sourcePath](#_bookmark543)                | A string that contains a list of items in the global ActionScript 3.0 Source path, which specifies the location of ActionScript class files. |
| [fl.spriteSheetExporter](#_bookmark545)       | Returns an instance of SpriteSheetExporter object.                                                                                           |
| [fl.swfPanels](#_bookmark546)                 | An array of registered swfPanel objects (see [swfPanel object](#_bookmark904)).                                                              |
| [fl.tools](#_bookmark549)                     | Read-only; an array of Tools objects.                                                                                                        |
| [fl.version](#_bookmark553)                   | Read-only; the long string version of the Flash authoring tool, including platform.                                                          |
| [fl.xmlui](#_bookmark556)                     | Read-only; an [XMLUI object](#_bookmark1151).                                                                                                |

<span id="fl.actionsPanel" class="anchor"></span>

