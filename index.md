---
title: Animate JSAPI Documentation
description: This is the home page of Animate APIs
---

# Animate JSAPI Documentation      
 

## Introduction

## Working with the JavaScript API

As a user of Adobe® Animate®, you may be familiar with Adobe® ActionScript®, which lets you create scripts that execute at run time in Adobe® Flash® Player. The Animate JavaScript application programming interface (JavaScript API or JSAPI) described in this document is a complementary programming tool that lets you create scripts that run in the Animate authoring environment.

This document describes the objects, methods, and properties available in the JavaScript API. It assumes that you know how to use the documented commands when working in the authoring environment. If you have a question about what a particular command does, use other documents in Animate Help, such as *Using Animate*, to find that information.

This document also assumes that you are familiar with JavaScript or ActionScript syntax and with basic programming concepts such as functions, parameters, and data types.

The Animate JavaScript API lets you write scripts to perform several actions in the Animate authoring environment (that is, while a user has the Animate program open). This functionality is different from the ActionScript language, which lets you write scripts to perform actions in the Flash Player environment (that is, while a SWF file is playing). This functionality is also different from JavaScript commands that you might use in pages displayed in a web browser.

Using the JavaScript API, you can write Animate application scripts to help streamline the authoring process. For example, you can write scripts to automate repetitive tasks or add custom tools to the Tools panel.

The Animate JavaScript API is designed to resemble the Adobe® Dreamweaver® and Adobe® Fireworks® JavaScript API (which were designed based on the Netscape JavaScript API). The Animate JavaScript API is based on a Document Object Model (DOM), which allows Animate documents to be accessed using JavaScript objects. The Animate JavaScript API includes all elements of the Netscape JavaScript API, plus the Animate DOM. These added objects and their methods and properties are described in this document. You can use any of the elements of the native JavaScript language in an Animate script, but only elements that make sense in the context of an Animate document have an effect.

The JavaScript API also contains methods that let you implement extensibility using a combination of JavaScript and custom C code. For more information, see [C-Level Extensibility](/C-Level_Extensibility/About_extensibility.md).

The JavaScript interpreter in Animate is the Mozilla SpiderMonkey engine, version 1.8, which is available on the web at [www.mozilla.org/js/spidermonkey/](http://www.mozilla.org/js/spidermonkey/). SpiderMonkey is one of the two reference implementations of the JavaScript language developed by Mozilla.org. It is the same engine that is embedded in the Mozilla browser.

SpiderMonkey implements the core JavaScript language as defined in the ECMAScript (ECMA-262) edition 3 language specification and it is fully compliant with the specification. Only the browser-specific host objects, which are not part of the ECMA-262 specification, are not supported. Similarly, many JavaScript reference guides distinguish between core JavaScript and client-side (browser-related) JavaScript. Only core JavaScript applies to the Animate JavaScript interpreter.

### Creating JSFL files

You can use Adobe Animate Professional or your preferred text editor to write and edit Animate JavaScript (JSFL) files. If you use Animate, these files have a .jsfl extension by default. To write a script, select File > New > Advanced > JSFL Script File.

You can also create a JSFL file by selecting commands in the History panel. Then click the Save button in the History panel or select Save As Command from the panel menu. The command (JSFL) file is saved in the Commands folder ([see Saving JSFL files](#saving-jsfl-files)). You can then open the file and edit it the same as any other script file.

The History panel provides some other useful options as well. You can copy selected commands to the Clipboard, and you can view JavaScript commands that are generated while you are working in Animate.

#### To copy commands from the History panel to the clipboard:

1.  Select one or more commands in the History panel.

2.  Do one of the following:

    -   Click the Copy button.

    -   Select Copy Steps from the panel menu.

#### To view JavaScript commands in the History panel:

-   Select View > JavaScript in Panel from the panel menu.

### Saving JSFL files

You can have JSFL scripts available within the Animate authoring environment by storing them in one of several folders within the Configuration folder. By default, the Configuration folder is in the following location:

-   Windows® 10™:

*boot drive*\\Users\\*username*\\AppData\\Local\\Adobe\\Animate *version*\\*language*\\Configuration\\

-   Mac OS® X:

Macintosh HD/Users/*username*/Library/Application Support/Adobe/Animate *version*/*language*/Configuration/

To determine the location of the Configuration folder, use [fl.configDirectory](/flash_object_(fl)/fl12.md) or [fl.configURI](/flash_object_(fl)/fl13.md), as shown in the following example:

```javascript
// store directory to a variable 
var configDir = fl.configDirectory;
// display directory in the Output panel 
fl.trace(fl.configDirectory);
```

Within the Configuration folder, the following folders can contain scripts that you can access in the authoring environment: Behaviors (to support the user interface for behaviors); Commands (for scripts that appear on the Commands menu); JavaScript (for scripts used by Script Assist to populate the user interface controls); Tools (for extensible tools in the Tools panel); and WindowSWF (for panels that appear in the Windows menu). This document focuses on scripts used for commands and tools.

If you edit a script in the Commands folder, the new script is immediately available in Animate. If you edit a script for an extensible tool, close and restart Animate, or else use the [fl.reloadTools()](flash_object_(fl)/fl57.md) command. However, if you used a script to add an extensible tool to the Tools panel and you then edit the script, either remove and then add the tool to the Tools panel again, or else close and restart Animate for the revised tool to be available.
There are two locations where you can store command and tool files so they can be accessed in the authoring environment.

-   For scripts that appear as items in the Commands menu, save the JSFL file in the Commands folder in the following location:

<table>
    <thead>
        <tr class="header">
            <th>
                <p><strong>Operating system</strong></p>
            </th>
            <th>
                <p><strong>Location</strong></p>
            </th>
        </tr>
    </thead>
    <tbody>
        <tr class="odd">
            <td>
                <p>Windows 10</p>
            </td>
            <td>
                <p><em>boot drive</em>\Users\<em>username</em>\AppData\Local\Adobe\Animate <em>version</em>\<em>language</em>\Configuration\Commands</p>
            </td>
        </tr>
        <tr class="even">
            <td>
                <p>Mac OS X</p>
            </td>
            <td>
                <p>Macintosh HD/Users/<em>userName</em>/Library/Application Support/Adobe/Animate <em>version/language</em>/Configuration/Commands</p>
            </td>
        </tr>
    </tbody>
</table>

-   For scripts that appear as extensible tools in the Tools panel, save the JSFL file in the Tools folder in the following location:

<table>
    <thead>
        <tr class="header">
            <th>
                <p><strong>Operating system</strong></p>
            </th>
            <th>
                <p><strong>Location</strong></p>
            </th>
        </tr>
    </thead>
    <tbody>
        <tr class="odd">
            <td>
                <p>Windows 10</p>
            </td>
            <td>
                <p><em>boot drive</em>\Users\<em>username</em>\AppData\Local\Adobe\Animate <em>version</em>\<em>language</em>\Configuration\Tools</p>
            </td>
        </tr>
        <tr class="even">
            <td>
                <p>Mac OS X</p>
            </td>
            <td>
                <p>Macintosh HD/Users/<em>userName</em>/Library/Application Support/Adobe/Animate <em>CC/language</em>/Configuration/Tools</p>
            </td>
        </tr>
    </tbody>
</table>

If a JSFL file has other files that go with it, such as XML files, store them in the same directory as the JSFL file.

### Running scripts

There are several ways to run scripts. The most common ways are explained in this section.

#### To run a script that you are currently viewing or editing:

-   Right-click (Command-click on the Macintosh) and choose Run Script.

-   Click the Run Script icon on the Script window toolbar.

This option lets you run a script before you have saved it. This option also lets you run a script even if no FLA files are open.

#### To run a script that is in the Commands folder, do one of the following:

-   From the authoring environment, select Commands > *Script Name*.

-   Use a keyboard shortcut that you have assigned to the script. To assign a keyboard shortcut, use Edit > Keyboard Shortcuts and select Drawing Menu Commands from the Commands pop-up menu. Expand the Commands node in the menu tree to view a list of available scripts.

#### To run a command script that is not in the Commands folder, do one of the following:

-   From the authoring environment, select Commands > Run Command, and then select the script to run.

-   From within a script, use the [fl.runScript()](flash_object_(fl)/fl62.md) command.

-   From the file system, double-click the script file.

#### To add a tool implemented in a JSFL file to the Tools panel:

1.  Copy the JSFL file for the tool and any other associated files to the Tools folder (see ["Saving JSFL files"](#saving-jsfl-files)).

2.  If tool is not visible in toolbar, click three dots (Edit Toolbar...)

3.  Add the tool to the list of available tools.

You can add individual JavaScript API commands to ActionScript files by using the MMExecute() function, which is documented in the *ActionScript 3.0 Language and Components Reference*. However, the MMExecute() function has an effect only when it is used in the context of a custom user interface element, such as a component Property inspector, or a SWF panel within the authoring environment. Even if called from ActionScript, JavaScript API commands have no effect in Flash Player or outside the authoring environment.

#### To issue a command from an ActionScript script:

-   Use the following syntax (you can concatenate several commands into one string):
```
MMExecute(Javascript command string);
```
You can also run a script from the command line.

#### To run a script from the command line on Windows:

-   Use the following syntax (add path information as required):
```
"Animate.exe" myTestFile.jsfl [-AlwaysRunJSFL]
```
Use the `-AlwaysRunJSFL` option to bypass the dialog box that prompts you to confirm script execution.

#### To run a script from the "Terminal" application on the Macintosh, use either of the following:

-   Use the following osacript syntax (add path information as required):
```
osascript -e 'tell application "Animate" to open alias "Mac OS X:Users:user:myTestFile.jsfl" '
```
The osascript command can also run AppleScript in a file. For example, you could include the following text in a file named myScript:
```
tell application "Animate"
open alias "Mac OS X:Users:user:myTestFile.jsfl" 
end tell
```
Then, to run the script, you would use this command:
osascript myScript

-   Use the Animate command:
```
/Applications/Adobe\ Animate\ 2020/Animate.app/Contents/MacOS/Animate \<path of the jsfl file\>
```



## What’s new in the JavaScript API

The following section lists new objects, methods, and properties in Animate. It also lists changes in Flash CC, CS6, CS5.5, and CS5.
If you have not used the JavaScript API before, you might want to skip this section and go directly to [JavaScript API objects](/Introduction/JavaScript_API_objects.md).

### New methods and properties in Animate 2020
The following methods and properties for existing objects are new in Animate 2020:

-   [Document object](../Document_object/document_summary.md)

    -   [document.getTaggedSwatches()](../Document_object/docu6064.md)

    -   [document.getTaggedSwatchByName()](../Document_object/docu6062.md)

    -   [document.getTaggedSwatchAtIndex()](../Document_object/docu6061.md)

    -   [document.setTaggedSwatchByName()](../Document_object/docu6068.md)

    -   [document.setTaggedSwatchAtIndex()](../Document_object/docu6067.md)

    -   [document.addTaggedSwatch()](../Document_object/docu6058.md)

    -   [document.addTaggedSwatchWithColor()](../Document_object/docu6059.md)

    -  [document.deleteTaggedSwatchByName()](../Document_object/docu6066.md)

    -   [document.deleteTaggedSwatchAtIndex()](../Document_object/docu6065.md)

    -   [document.getTaggedSwatchesPaletteList()](../Document_object/docu6063.md)

    -   [document.getIndexForTaggedSwatchesPalette()](../Document_object/docu6060.md)

    -   [document.convertToDoc()](../Document_object/docu6069.md)

    -   [document.exportCanvasPublishTemplate()](../Document_object/docu6070.md)

    -   [document.importCanvasPublishTemplate()](../Document_object/docu6071.md)

    -  [document.exportMedia()](../Document_object/docu6072.md)

    -   [document.exportSVG()](../Document_object/docu6074.md)

-   [Layer object](../Layer_object/layer_summary.md)

    -   [layer.getZDepthAtFrame()](../Layer_object/layer11.md)

    -   [layer.setZDepthAtFrame()](../Layer_object/layer12.md)

    -   [layer.getRigParentAtFrame()](../Layer_Parenting_Object/layerParenting1.md)

    -   [layer.setRigParentAtFrame()](../Layer_Parenting_Object/layerParenting2.md)

    -   [layer.getRigMatrixAtFrame()](../Layer_Parenting_Object/layerParenting3.md)

    -   [layer.getFiltersAtFrame()](../Layer_object/layer15.md)

    -   [layer. setFiltersAtFrame()](../Layer_object/layer18.md)

    -   [layer.getColorTransformAtFrame()](../Layer_object/layer14.md)

    -   [layer.setColorTransformAtFrame()](../Layer_object/layer17.md)

    -   [layer.getBlendModeAtFrame()](../Layer_object/layer13.md)

    -   [layer.setBlendModeAtFrame()](../Layer_object/layer16.md)

-   [Timeline object](../Timeline_object/timeline_summary.md)

    -   [timeline.advancedLayersEnabled](../Timeline_object/timeli52.md)

    -   [timeline.mergeLayers()](../Timeline_object/timeli51.md)

-   [flash object (fl)](../flash_object_(fl)/fl_summary.md)

    -   [fl.addToolInToolbar()](../flash_object_(fl)/fl82.md)


### New objects in Animate 2020
The following object is new in Flash CS6:

-   [TextureAtlasExporter object](../TextureAtlasExporter_object/TextureAtlasExporter_summary.md)

-   [Camera object](../Camera_object/Camera_Summary.md)

### New methods and properties in Flash CC

The following methods and properties for existing objects are new in Flash Profesional CC:

-   [Tween Object](../Tween_Object/Tween_object_Summary.md)

    -   Tween.getColorTransform( )

    -   Tween.getFilters( )

    -   Tween.getGeometricTransform()

    -   Tween.getShape( )

    -   Tween.duration

    -   Tween.startFrame

    -   Tween.tweenType

-   [CompiledClipInstance object](../CompiledClipInstance_object/compiledClipInstance_summary.md)

    -   CompiledClipInstance.backgroundColor

    -   CompiledClipInstance.blendMode

    -   CompiledClipInstance.brightness

    -   CompiledClipInstance.cacheAsBitmap

    -   CompiledClipInstance.colorAlphaAmount

    -   CompiledClipInstance.colorAlphaPercent

    -   CompiledClipInstance.colorBlueAmount

    -   CompiledClipInstance.colorBluePercent

    -   CompiledClipInstance.colorGreenAmount

    -   CompiledClipInstance.colorGreenPercent

    -   CompiledClipInstance.colorMode

    -   CompiledClipInstance.colorRedAmount

    -   CompiledClipInstance.colorRedPercent

    -   CompiledClipInstance.filters

    -   CompiledClipInstance.tintColor

    -   CompiledClipInstance.tintPercent

    -   CompiledClipInstance.useBackgroundColor

    -   CompiledClipInstance.visible

-   [Document object](../Document_object/document_summary.md)

    -   Document.convertSelectionToBitmap()

    -   Document.distributeToKeyframes()

    -   Document.exportVideo()

    -   Document.getPublishDocumentData()

    -   Document.getTelemetryForSwf()

    -   Document.importFile() showDialog and showImporterUI properties

    -   Document.setPublishDocumenData()

-   [Element object](../Element_object/element_summary.md)

    -   Element.getPublishPersistentData()

    -   Element.setPublishPersistentData()

-   [flash object (fl)](../flash_object_(fl)/fl_summary.md)

    -   Flash.addEventListener()prePublish, postPublish, selectionChanged, and dpiChanged events

    -   fl.getThemeColor()

    -   fl.getThemeColorParameters()

    -   fl.getThemeFontInfo()

    -   fl.setPrefBoolean()

    -   fl.toggleBreakPoint()

    -   fl.xmlPanel()

    -   fl.xmlPanelFromString()

-   [Frame object](../Frame_object/frame_summary.md)

    -   Frame.convertToFrameByFrameAnimation()

    -   Frame.getSoundEnvelope()

    -   Frame.getSoundEnvelopeLimits()

    -   Frame.setSoundEnvelope()

    -   Frame.setSoundEnvelopeLimits()

    -   Frame.isEmpty()

-   [Item object](../Item_object/item_summary.md)

    -   item.getPublishData()

    -   item.setPublishData()

-   [library object](../library_object/library_summary.md)

    -   library.unusedItems

-   [swfPanel object](../swfPanel_object/swfPanel_summary.md)

    -   swfPanel.dpiScaleFactorX

    -   swfPanel.dpiScaleFactorY

    -   swfPanel.reload()

-   [SymbolInstance object](../SymbolInstance_object/symbolInstance_summary.md)

    -   SymbolInstance.brightness

    -   SymbolInstance.tintColor

    -   SymbolInstance.tintPercent

-   [Timeline object](../Timeline_object/timeline_summary.md)

    -   getBounds()

### Dropped methods and properties in Flash CC

The following methods and properties for existing objects are dropped in Adobe Animate:

-   ActionsPanel.getClassForObject()

-   ActionsPanel.getScriptAssistMode()

-   ActionsPanel.setScriptAssistMode()

-   CompiledClipInstance.actionscript

-   fl.reloadEffects()

-   fl.resetPackagePaths()

-   document.activeEffect

-   document.allowScreens()

-   document.drawingLayer

-   document.importSWF()

-   document.loadCuePointXML()

-   document.packagePaths

-   document.saveAndCompact()

-   document.screenType

-   library.importEmbeddedSWF()

-   SymbolInstance.actionscript

### New objects in Flash CS6

The following object is new in Flash CS6:

-   [SpriteSheetExporter object](../SpriteSheetExporter_object/SpriteSheetExporter_summary.md)

### New methods and properties in Flash CS6

The following methods and properties for existing objects are new in Flash Pro CS6:

-   [BitmapItem object](../BitmapItem_object/bitmapItem_summary.md)

    -   bitmapItem.exportToFile()quality parameter

    -   bitmapItem.hasValidAlphaLayer

    -   bitmapItem.lastModifiedDate

-   [Document object](../Document_object/document_summary.md)

    -   document.exportInstanceToLibrary()

    -   document.exportInstanceToPNGSequence()

    -   document.getSWFPathFromProfile()

    -   document.saveAsCopy()

    -   document.swfJPEGQuality

-   [flash object (fl)](../flash_object_(fl)/fl_summary.md)

    -   fl.spriteSheetExporter

-   [Layer object](../Layer_object/layer_summary.md)

    -   layer.animationType

-   [Math object](../Math_object/Math_summary.md)

    -   Math.transformPoint()

-   [Shape object](../Shape_object/shape_summary.md)

    -   shape.isFloating

-   [SoundItem object](../SoundItem_object/soundItem_summary.md)

    -   soundItem.lastModifiedDate

-   [SymbolInstance object](../SymbolInstance_object/symbolInstance_summary.md)

    -   symbolInstance.is3D

-   [SymbolItem object](../SymbolItem_object/symbolItem_summary.md)

    -   symbolItem.exportToLibrary()

    -   symbolItem.exportToPNGSequence()

    -   symbolItem.lastModifiedDate

-   [Text object](../Text_object/text_summary.md)

    -   text.filters

-   [VideoItem object](../VideoItem_object/videoItem_summary.md)

    -   videoItem.lastModifiedDate

### New methods and properties in Flash CS5 and CS5.5

The following methods and properties for existing objects are new in Flash Pro CS5:

-   [Document object](../Document_object/document_summary.md)

    -   document.debugMovie()

    -   document.loadCuepointXML()

-   [flash object (fl)](../flash_object_(fl)/fl_summary.md)

    -   fl.languageCode

    -   fl.toggleBreakpoint

-   [Frame object](../Frame_object/frame_summary.md)

    -   frame.convertMotionObjectTo2D()

    -   frame.convertMotionObjectTo3D()

    -   frame.getMotionObjectXML()

    -   frame.hasMotionPath()

    -   frame.isMotionObject()

    -   frame.is3DMotionObject()

    -   frame.selectMotionPath()

    -   frame.setMotionObjectDuration()

    -   frame.setMotionObjectXML()

    -   frame.tweenInstanceName

-   [Timeline object](../Timeline_object/timeline_summary.md)

    -   timeline.createMotionObject()

    -   timeline.libraryItem

    -   timeline.removeMotionObject()

    -   timeline.startPlayback

    -   timeline.stopPlayback

The following methods and properties for existing objects are new in Flash Pro CS5.5:

-   [SymbolInstance object](../SymbolInstance_object/symbolInstance_summary.md)

    -   symbolInstance.bitmapRenderMode

    -   symbolInstance.backgroundColor

    -   symbolInstance.usesBackgroundColor

    -   symbolInstance.visible

-   [Timeline object](../Timeline_object/timeline_summary.md)

    -   timeline.copyLayers()

    -   timeline.cutLayers()

    -   timeline.duplicateLayers()

    -   timeline.pasteLayers()

-   [flash object (fl)](../flash_object_(fl)/fl_summary.md)

    -   fl.getSwfPanel()

    -   fl.installedPlayers()

    -   fl.publishCacheEnabled

    -   fl.publishCacheDiskSizeMax

    -   fl.publishCacheMemorySizeMax

    -   fl.publishCacheMemoryEntrySizeLimit

    -   fl.clearPublishCache()

-   [swfPanel object](../swfPanel_object/swfPanel_summary.md)

    -   swfPanel.setFocus()

### Other changes in Flash CS5 and CS5.5

The following methods and properties are updated in Flash CS5:

-   fl.openScript()

-   fl.publishDocument()

-   fontItem.embedRanges

-   fontItem.embeddedCharacters

-   fontItem.embedVariantGlyphs

The following objects and method are no longer available in Flash CS5:

-   Screen object

-   ScreenOutline object

-   document.canSaveAVersion()

-   document.revertToLastVersion()

-   document.saveAVersion()

-   document.synchronizeWithHeadVersion()

-   fl.downloadLatestVersion()

-   fl.revertDocumentToLastVersion()

-   fl.saveAVersionOfDocument()

-   fl.synchronizeDocumentWithHeadVersion()





## JavaScript API objects

This section provides a summary of the objects available in the Animate JavaScript API and how to begin working with them. All standard JavaScript commands are also available when working with the JavaScript API.

The following table briefly describes each of the objects in the JavaScript API. The objects are listed in alphabetical order.

| **Object**                  | **Description**                                                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| actionsPanel object         | The actionsPanel object represents the currently displayed Actions panel.                                                    |
| BitmapInstance object       | The BitmapInstance object is a subclass of the Instance object and represents a bitmap in a frame.                           |
| BitmapItem object           | A BitmapItem object refers to a bitmap in the library of a document. The BitmapItem object is a subclass of the Item object. |
| CompiledClipInstance object | The CompiledClipInstance object is a subclass of the Instance object.                                                        |
| compilerErrors object       | The compilerErrors object represents the Compiler Errors panel. It is a property of the flash object (```fl.compilerErrors```).    |
| ComponentInstance object    | The ComponentInstance object is a subclass of the SymbolInstance object and represents a component in a frame.               |
| componentsPanel object      | The componentsPanel object, which represents the Components panel, is a property of the flash object (```fl.componentsPanel```).   |
| Contour object              | A Contour object represents a closed path of half edges on the boundary of a shape.                                          |
| Document object             | The Document object represents the Stage.                                                                                    |
| drawingLayer object         | The drawingLayer object is accessible from JavaScript as a child of the flash object.                                        |
| Edge object                 | The Edge object represents an edge of a shape on the Stage.                                                                  |
| Element object              | Everything that appears on the Stage is of the type Element.                                                                 |
| Fill object                 | The Fill object contains all the properties of the Fill color setting of the Tools panel or of a selected shape.             |

| **Object**            | **Description**                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter object         | The Filter object contains all the properties for all filters.                                                                                                                                                                                                                      |
| flash object (fl)     | The flash object represents the Animate application.                                                                                                                                                                                                                                  |
| FLfile object         | The FLfile object lets you write Animate extensions that can access, modify, and remove files and folders on the local file system.                                                                                                                                                   |
| folderItem object     | The folderItem object is a subclass of the Item object.                                                                                                                                                                                                                             |
| fontItem object       | The fontItem object is a subclass of the Item object.                                                                                                                                                                                                                               |
| Frame object          | The Frame object represents frames in the layer.                                                                                                                                                                                                                                    |
| HalfEdge object       | Directed side of the edge of a Shape object.                                                                                                                                                                                                                                        |
| Instance object       | The Instance object is a subclass of the Element object.                                                                                                                                                                                                                            |
| Item object           | The Item object is an abstract base class.                                                                                                                                                                                                                                          |
| Layer object          | The Layer object represents a layer in the timeline.                                                                                                                                                                                                                                |
| library object        | The library object represents the Library panel.                                                                                                                                                                                                                                    |
| Math object           | The Math object is available as a read-only property of the flash object (```fl.Math```).                                                                                                                                                                                                 |
| Matrix object         | The Matrix object represents a transformation matrix.                                                                                                                                                                                                                               |
| outputPanel object    | The outputPanel object represents the Output panel, which displays troubleshooting information such as syntax errors. It is a property of the flash object (```fl.outputPanel```).                                                                                                        |
| Oval object           | The Oval object is a shape that is drawn using the Oval tool. To determine if an item is an Oval object, use ```shape.isOvalObject```.                                                                                                                                                    |
| Parameter object      | The Parameter object type is accessed from the screen.parameters array (which corresponds to the screen Property inspector in the Animate authoring tool) or by the componentInstance.parameters array (which corresponds to the component Property inspector in the authoring tool). |
| Path object           | The Path object defines a sequence of line segments (straight, curved, or both), which you typically use when creating extensible tools.                                                                                                                                            |
| presetItem object     | The presetItem object represents an item (preset or folder) in the Motion Presets panel.                                                                                                                                                                                            |
| presetPanel object    | The presetPanel object represents the Motion Presets panel (Window > Motion Presets). It is a property of the flash object (```fl.presetPanel```).                                                                                                                                       |
| Rectangle object      | The Rectangle object is a shape that is drawn using the Rectangle tool. To determine if an item is a Rectangle object, use shape.isRectangleObject.                                                                                                                                 |
| Screen object         | The Screen object represents a single screen in a slide or form document.                                                                                                                                                                                                           |
| ScreenOutline object  | The ScreenOutline object represents the group of screens in a slide or form document.                                                                                                                                                                                               |
| Shape object          | The Shape object is a subclass of the Element object. The Shape object provides more precise control than the drawing APIs for manipulating or creating geometry on the Stage.                                                                                                      |
| SoundItem object      | The SoundItem object is a subclass of the Item object. It represents a library item used to create a sound.                                                                                                                                                                         |
| Stroke object         | The Stroke object contains all the settings for a stroke, including the custom settings.                                                                                                                                                                                            |
| swfPanel object       | The swfPanel object represents a Windows SWF panel. Windows SWF panels are SWF files that implement applications you can run from the Animate authoring environment. The array of swfPanel objects is a property of the flash object (```fl.swfPanels```).                                  |
| SymbolInstance object | The SymbolInstance object is a subclass of the Instance object and represents a symbol in a frame.                                                                                                                                                                                  |

| **Object**        | **Description**                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| SymbolItem object | The SymbolItem object is a subclass of the Item object.                                                                                       |
| Text object       | The Text object represents a single text item in a document.                                                                                  |
| TextAttrs object  | The TextAttrs object contains all the properties of text that can be applied to a subselection. This object is a subclass of the Text object. |
| TextRun object    | The TextRun object represents a run of characters that have attributes that match all of the properties in the TextAttrs object.              |
| Timeline object   | The Timeline object represents the Animate timeline, which can be accessed for the current document by ```fl.getDocumentDOM().getTimeline()```.       |
| ToolObj object    | A ToolObj object represents an individual tool in the Tools panel.                                                                            |
| Tools object      | The Tools object is accessible from the Flash object (```fl.tools```).                                                                              |
| Vertex object     | The Vertex object is the part of the shape data structure that holds the coordinate data.                                                     |
| VideoItem object  | The VideoItem object is a subclass of the Item object.                                                                                        |
| XMLUI object      | The XMLUI object provides the ability to get and set properties of an XMLUI dialog box, and accept or cancel out of one.                      |

### The Animate Document Object Model

The Animate Document Object Model (DOM) for the Animate JavaScript API consists of a set of top-level functions (see ["Top-Level Functions and Methods"](../Top-Level_Functions_and_Methods/Top.md)) and two top-level objects—the FLfile object and the flash object (an or fl). Each object is guaranteed to be available to a script because it always exists when the Animate authoring environment is open. For more information, see [FLfile object](../FLfile_object/FLfile_summary.md) and [flash object (fl)](../flash_object_(fl)/fl_summary.md).
When referring to the flash object, you can use flash or an or fl. For example, to close all open FLA files, you can use either of the following statements:
```javascript
flash.closeAll(); 
an.closeAll();
fl.closeAll();
```
The flash object contains the following *child objects*:

| **Object**             | **How to access**                                                                                                                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| actionsPanel object    | Use ```fl.actionsPanel``` to access the actionsPanel object. This object corresponds to the Actions panel in the Animate authoring environment.                                                                  |
| compilerErrors object  | Use ```fl.compilerErrors``` to access the compilerErrors object. This object corresponds to the Compiler Errors panel in the Animate authoring environment.                                                      |
| componentsPanel object | Use ```fl.componentsPanel``` to access the componentsPanel object. This object corresponds to the Components panel in the Animate authoring environment.                                                         |
| Document object        | Use ```fl.documents``` to retrieve an array of all the open documents; use ```fl.documents[index]``` to access a particular document; use ```fl.getDocumentDOM()``` to access the current document (the one with focus). |
| drawingLayer object    | Use ```fl.drawingLayer``` to access the drawingLayer object.                                                                                                                                                   |
| Math object            | Use ```fl.Math``` to access the Math object.                                                                                                                                                                   |
| outputPanel object     | Use ```fl.outputPanel``` to access the outputPanel object. This object corresponds to the Output panel in the Animate authoring environment.                                                                     |

| **Object**         | **How to access**                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| presetPanel object | Use ```fl.presetPanel``` to access the presetPanel object. This object corresponds to the Motion Presets panel (Window > Motion Presets).                 |
| swfPanel object    | Use ```fl.swfPanels``` to access an array of swfPanel objects. These objects correspond to Window SWF panels.                                              |
| Tools object       | Use ```fl.tools``` to access an array of Tools objects.                                                                                                    |
| XMLUI object       | Use ```fl.xmlui``` to access an XML User Interface (XMLUI) object. The XMLUI object provides the ability to get and set properties of an XMLUI dialog box. |

### The Document object

An important property of the top-level flash object is the [fl.documents](../flash_object_(fl)/fl20.md) property. This property contains an array of Document objects, each of which represents one of the FLA files currently open in the authoring environment. The properties of each Document object represent most of the elements that a FLA file can contain. Therefore, a large portion of the DOM is composed of child objects and properties of the Document object. For more information, see [Document object](../Document_object/document_summary.md).

To refer to the first open document, for example, use the statement ```flash.documents[0]``` or ```fl.documents[0]```. The first document is the first Animate document that was opened during the current session in the authoring environment. When the first opened document is closed, the indexes of the other open documents are decremented.

To find a particular document’s index, use ```flash.findDocumentIndex(nameOfDocument)``` or ```fl.findDocumentIndex(nameOfDocument)```. See [fl.findDocumentIndex()](../flash_object_(fl)/fl26.md).

To access the document that is currently focused, use the statement ```flash.getDocumentDOM()``` or ```fl.getDocumentDOM()```. See [fl.getDocumentDOM()](../flash_object_(fl)/fl31.md). The latter is the syntax used in most of the examples in this document.

To find a particular document in the fl.documents array, iterate through the array and test each document for its
```document.name``` property. See [fl.documents](../flash_object_(fl)/fl20.md) and [document.name](../Document_object/docum170.md).

All the objects in the DOM that aren’t listed in the previous table (see ["The Animate Document Object Model"](#the-animate-document-object-model)) are accessed from the Document object. For example, to access the library of a document, you use the ```document.library``` property, which retrieves a library object:

```fl.getDocumentDOM().library```

To access the array of items in the library, you use the ```library.items``` property; each element in the array is an Item object:

```fl.getDocumentDOM().library.items```

To access a particular item in the library, you specify a member of the library.items array:

```fl.getDocumentDOM().library.items[0]```

In other words, the library object is a child of the Document object, and the Item object is a child of the library object. For more information, see [document.library](../Document_object/docume98.md), [library object](../library_object/library_summary.md), [library.items](../library_object/librar10.md) and [Item object](../Item_object/item_summary.md).

### Specifying the target of an action

Unless otherwise specified, methods affect the current focus or selection. For example, the following script doubles the size of the current selection because no particular object is specified:

```fl.getDocumentDOM().scaleSelection(2, 2);```

In some cases, you might want an action to specifically target the currently selected item in the Animate document. To do this, use the array that the ```document.selection``` property contains (see [document.selection](../Document_object/docum430.md)). The first element in the array represents the currently selected item, as shown in the following example:

```var accDescription = fl.getDocumentDOM().selection[0].description;```

The following script doubles the size of the first element on the Stage that is stored in the element array, instead of the current selection:
```javascript
var element = fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0];
if (element) {
    element.width = element.width*2; 
    element.height = element.height*2;
}
```
You can also do something such as loop through all the elements on the Stage and increase the width and height by a specified amount, as shown in the following example:
```javascript
var elementArray = fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements;
for (var i=0; i < elementArray.length; i++) {
    var offset = 10;
    elementArray[i].width += offset; 
    elementArray[i].height += offset;
}
```
### Summary of the DOM structure

The following list displays the DOM structure in outline format. Numbers at the beginning of each line represent the level of an object. For example, an object preceded by "03" is a child of next highest "02" object, which, in turn, is a child of the next highest "01" object.

In some cases, an object is available by specifying a property of its parent object. For example, the ```document.timelines``` property contains an array of Timeline objects. These properties are noted in the following outline.

Some objects are subclasses of other objects, rather than being children of other objects. An object that is a subclass of another object has methods and/or properties of its own in addition to the methods and properties of the parent object (the superclass). Subclasses share the same level in the hierarchy as their superclass. For example, the Item object is a superclass of the BitmapItem object. These relationships are illustrated in the following outline:

```
01 Top-Level Functions and Methods 
01 FLfile object
01 flash object (fl)
    02 compilerErrors object
    02 componentsPanel object
    02 Document object (fl.documents array) 
        03 Filter object
        03 Matrix object
        03 Fill object
        03 Stroke object
        03 library object
            04 Item object (library.items array)
            04 BitmapItem object(subclass of Item object) 
            04 folderItem object (subclass of Item object) 
            04 fontItem object (subclass of Item object) 
            04 SoundItem object (subclass of Item object) 
            04 SymbolItem object (subclass of Item object) 
            04 VideoItem object (subclass of Item object)
        03 Timeline object (document.timelines array) 
            04 Layer object (timeline.layers array)
                05 Frame object (layer.frames array)
                    06 Element object (frame.elements array) 
                        07 Matrix object (element.matrix)
                    06 Instance object (abstract class, subclass of Element object) 
                    06 BitmapInstance object (subclass of Instance object)
                    06 CompiledClipInstance object (subclass of Instance object)
                    06 ComponentInstance object (subclass of SymbolInstance object) 
                        07 Parameter object (componentInstance.parameters array)
                    06 SymbolInstance object (subclass of Instance object) 
                    06 Text object (subclass of Element object)
                        07 TextRun object (text.textRuns array)
                            08 TextAttrs object (textRun.textAttrs array) 
                    06 Shape object (subclass of Element object)
                        07 Oval object
                        07 Rectangle object
                        07 Contour object (shape.contours array) 
                            08 HalfEdge object
                                09 Vertex object
                                09 Edge object
                        07 Edge object (shape.edges array) 
                            08 HalfEdge object
                                09 Vertex object
                                09 Edge object
                        07 Vertex object(shape.vertices array)
                            08 HalfEdge object
                                09 Vertex object
                                09 Edge object
                05 Parameter object (screen.parameters array) 
    02 drawingLayer object
        03 Path object
            04 Contour object
    02 Math object
    02 outputPanel object
    02 presetPanel object
        03 presetItem object(presetPanel.items array) 
    02 swfPanel object
    02 Tools object (fl.tools array)
        03 ToolObj object (tools.toolObjs array) 
    02 XMLUI object
```

## Sample implementations

Several sample JSFL implementations are available for Adobe Animate. You can review and install these files to familiarize yourself with the JavaScript API. The samples are in a folder named Samples within the [Samples.zip](https://github.com/AdobeDocs/developers-animatesdk-docs/raw/master/downloads/Samples.zip).

### Sample Shape command

A sample JavaScript API script named Shape.jsfl is located in the Shape folder (see "Sample implementations" above). This script displays information about the contours of the shape in the Output panel.

#### To install and run the Shape script:

1.  Copy the Shape.jsfl file to the Configuration > Commands folder (see ["Saving JSFL files"](/Introduction/Working_with_the_JavaScript_API.md#saving-jsfl-files)).

2.  In a Animate document (FLA file), select a shape object.

3.  Select Commands > Shape to run the script.

### Sample get and set filters command

A sample JavaScript API script named filtersGetSet.jsfl is located in the filtersGetSet folder (see "Sample implementations" above). This script adds filters to a selected object and displays information about the filters being added in the Output panel.

#### To install and run the filtersGetSet script:

1.  Copy the filtersGetSet.jsfl file to the Configuration/Commands folder (see ["Saving JSFL files"](/Introduction/Working_with_the_JavaScript_API.md#saving-jsfl-files)).

2.  In a Animate document (FLA file), select a text, movie clip, or button object.

3.  Select Commands > filtersGetSet to run the script.

### Sample PolyStar tool

A sample JavaScript API script named PolyStar.jsfl is located in the PolyStar folder (see "Sample implementations" above).
The PolyStar.jsfl replicates the PolyStar tool that can be found in the Animate Tools panel. The script demonstrates how to build the PolyStar tool using the JavaScript API and includes detailed comments describing what the code is doing. Read this file to gain a better understanding of how the JavaScript API can be used. You should also read the PolyStar.xml file in the Tools directory to learn more about how to build your own tool.

### Sample Trace Bitmap panel

A set of files named TraceBitmap.fla and TraceBitmap.swf are located in the TraceBitmapPanel folder (see "Sample implementations" above). These files illustrate how to design and build a panel to control the functions of Animate. They also show the use of the MMExecute() function to call JavaScript commands from an ActionScript script.

#### To run the TraceBitmap sample:

1.  If Animate is running, exit from Animate.

2.  Copy the TraceBitmap.swf file to the WindowSWF folder, which is a subdirectory of the Configuration folder (see ["Saving JSFL files"](/Introduction/Working_with_the_JavaScript_API.md#saving-jsfl-files)). For example, on Windows 10, the folder is in *boot drive*\\Users\\*username*\\AppData\\Local\\Adobe\\Animate 2020\\*language*\\Configuration\\WindowSWF.

3.  Start Animate.

4.  Create or open a Animate document (FLA file), and import a bitmap or JPEG image into the file.

You can use the flower.jpg file provided in the TraceBitmapPanel folder or another image of your choice.

1.  With the imported image selected, select Window > Other Panels > TraceBitmap.

2.  Click Submit.

The image is converted into a group of shapes.

### Sample DLL

A sample DLL implementation is located in the dllSampleComputeSum folder (see "Sample implementations" above). For more information about building DLLs, see[ "C-Level Extensibility"](../C-Level_Extensibility/About_extensibility.md).




## Top-LevelFunctionsandMethods

[Top-levelsummary](./Top-Level_Functions_and_Methods/Top.md)

[activate()](./Top-Level_Functions_and_Methods/activate.md)

[alert()](./Top-Level_Functions_and_Methods/alert.md)

[configureTool()](./Top-Level_Functions_and_Methods/configureTool.md)

[confirm()](./Top-Level_Functions_and_Methods/confirm.md)

[deactivate()](./Top-Level_Functions_and_Methods/deactivate.md)

[keyDown()](./Top-Level_Functions_and_Methods/keyDown.md)

[keyUp()](./Top-Level_Functions_and_Methods/keyUp.md)

[mouseDoubleClick()](./Top-Level_Functions_and_Methods/mouseDoubleClick.md)

[mouseDown()](./Top-Level_Functions_and_Methods/mouseDown.md)

[mouseMove()](./Top-Level_Functions_and_Methods/mouseMove.md)

[mouseUp()](./Top-Level_Functions_and_Methods/mouseUp.md)

[notifySettingsChanged()](./Top-Level_Functions_and_Methods/notifySettingsChanged.md)

[prompt()](./Top-Level_Functions_and_Methods/prompt.md)

[setCursor()](./Top-Level_Functions_and_Methods/setCursor.md)


## actionsPanelObject

[actionsPanelsummary](./actionsPanel_object/actionsPanel_summary.md)

[actionsPanel.getClassForObject.md)-dropped](./actionsPanel_object/actionsPanel.md)

[actionsPanel.getScriptAssistMode.md)-dropped](./actionsPanel_object/actionsPane1.md)

[actionsPanel.getSelectedText()](./actionsPanel_object/actionsPane2.md)

[actionsPanel.getText()](./actionsPanel_object/actionsPane3.md)

[actionsPanel.hasSelection()](./actionsPanel_object/actionsPane4.md)

[actionsPanel.replaceSelectedText()](./actionsPanel_object/actionsPane5.md)

[actionsPanel.setScriptAssistMode.md)-dropped](./actionsPanel_object/actionsPane6.md)

[actionsPanel.setSelection()](./actionsPanel_object/actionsPane7.md)

[actionsPanel.setText()](./actionsPanel_object/actionsPane8.md)


## bitmapInstanceObject

[bitmapInstancesummary](./BitmapInstance_object/bitmapInstance_summary.md)

[bitmapInstance.getBits()](./BitmapInstance_object/bitmapInstance.md)

[bitmapInstance.hPixels](./BitmapInstance_object/bitmapInstanc1.md)

[bitmapInstance.setBits()](./BitmapInstance_object/bitmapInstanc2.md)

[bitmapInstance.vPixels](./BitmapInstance_object/bitmapInstanc3.md)


## bitmapItemObject

[bitmapItemsummary](./BitmapItem_object/bitmapItem_summary.md)

[bitmapItem.allowSmoothing](./BitmapItem_object/bitmapItem.md)

[bitmapItem.compressionType](./BitmapItem_object/bitmapIte1.md)

[bitmapItem.exportToFile()](./BitmapItem_object/bitmapIte2.md)

[bitmapItem.fileLastModifiedDate](./BitmapItem_object/bitmapIte3.md)

[bitmapItem.hasValidAlphaLayer](./BitmapItem_object/bitmapIte4.md)

[bitmapItem.hPixels](./BitmapItem_object/bitmapIte5.md)

[bitmapItem.lastModifiedDate](./BitmapItem_object/bitmapIte6.md)

[bitmapItem.originalCompressionType](./BitmapItem_object/bitmapIte7.md)

[bitmapItem.quality](./BitmapItem_object/bitmapIte8.md)

[bitmapItem.sourceFileExists](./BitmapItem_object/bitmapIte9.md)

[bitmapItem.sourceFileIsCurrent](./BitmapItem_object/bitmapIt10.md)

[bitmapItem.sourceFilePath](./BitmapItem_object/bitmapIte11.md)

[bitmapItem.useDeblocking](./BitmapItem_object/bitmapIte12.md)

[bitmapItem.useImportedJPEGQuality](./BitmapItem_object/bitmapIte13.md)

[bitmapItem.vPixels](./BitmapItem_object/bitmapIte14.md)


## CameraObject

[Camerasummary](./Camera_object/Camera_Summary.md)

[getColorFilter())](./Camera_object/Camera5.md)

[getPosition()](./Camera_object/Camera3.md)

[getRotation()](./Camera_object/Camera2.md)

[getTint()](./Camera_object/Camera4.md)

[getZDepth()](./Camera_object/Camera.md)

[getZoom()](./Camera_object/Camera1.md)

[reset()](./Camera_object/Camera16.md)

[resetColorFilter()](./Camera_object/Camera15.md)

[resetPosition()](./Camera_object/Camera13.md)

[resetRotation()](./Camera_object/Camera12.md)

[resetTint()](./Camera_object/Camera14.md)

[resetZoom()](./Camera_object/Camera11.md)

[setColorFilter()](./Camera_object/Camera10.md)

[setRotation()](./Camera_object/Camera8.md)

[setTint()](./Camera_object/Camera9.md)

[setZDepth()](./Camera_object/Camera6.md)

[setZoom()](./Camera_object/Camera7.md)

[camera.cameraEnabled](./Camera_object/Camera17.md)

[camera.colorFilterEnabled](./Camera_object/Camera19.md)

[camera.tintEnabled](./Camera_object/Camera18.md)


## compiledClipInstanceObject

[compiledClipInstancesummary](./CompiledClipInstance_object/compiledClipInstance_summary.md)

[compiledClipInstance](./CompiledClipInstance_object/compiledClipInstance.md)

[compiledClipInstance.actionScript-dropped](./CompiledClipInstance_object/compiledClipInstanc1.md)

[compiledClipInstance.backgroundColor](./CompiledClipInstance_object/compiledClipInstanc2.md)

[compiledClipInstance.blendMode](./CompiledClipInstance_object/compiledClipInstanc3.md)

[compiledClipInstance.brightness](./CompiledClipInstance_object/compiledClipInstanc4.md)

[compiledClipInstance.cacheAsBitmap](./CompiledClipInstance_object/compiledClipInstanc5.md)

[compiledClipInstance.colorAlphaAmount](./CompiledClipInstance_object/compiledClipInstanc6.md)

[compiledClipInstance.colorAlphaPercent](./CompiledClipInstance_object/compiledClipInstanc7.md)

[compiledClipInstance.colorBlueAmount](./CompiledClipInstance_object/compiledClipInstanc8.md)

[compiledClipInstance.colorBluePercent](./CompiledClipInstance_object/compiledClipInstanc9.md)

[compiledClipInstance.colorGreenAmount](./CompiledClipInstance_object/compiledClipInstan10.md)

[compiledClipInstance.colorGreenPercent](./CompiledClipInstance_object/compiledClipInstan11.md)

[compiledClipInstance.colorMode](./CompiledClipInstance_object/compiledClipInstan12.md)

[compiledClipInstance.colorRedAmount](./CompiledClipInstance_object/compiledClipInstan13.md)

[compiledClipInstance.colorRedPercent](./CompiledClipInstance_object/compiledClipInstan14.md)

[compiledClipInstance.description](./CompiledClipInstance_object/compiledClipInstan15.md)

[compiledClipInstance.filters](./CompiledClipInstance_object/compiledClipInstan16.md)

[compiledClipInstance.forceSimple](./CompiledClipInstance_object/compiledClipInstan17.md)

[compiledClipInstance.shortcut](./CompiledClipInstance_object/compiledClipInstan18.md)

[compiledClipInstance.silent](./CompiledClipInstance_object/compiledClipInstan19.md)

[compiledClipInstance.tabIndex](./CompiledClipInstance_object/compiledClipInstan20.md)

[compiledClipInstance.tintColor](./CompiledClipInstance_object/compiledClipInstan21.md)

[compiledClipInstance.tintPercent](./CompiledClipInstance_object/compiledClipInstan22.md)

[compiledClipInstance.useBackgroundColor](./CompiledClipInstance_object/compiledClipInstan23.md)

[compiledClipInstance.visible](./CompiledClipInstance_object/compiledClipInstan24.md)


## compilerErrorsObject

[compilerErrorssummary](./compilerErrors_object/compilerErrors_summary.md)

[compilerErrors.clear()](./compilerErrors_object/compilerErrors.md)

[compilerErrors.save()](./compilerErrors_object/compilerError1.md)


## componentInstanceObject

[componentInstancesummary](./ComponentInstance_object/componentInstance_summary.md)

[componentInstance.parameters](./ComponentInstance_object/componentInstance.md)


## componentsPanelObject

[componentsPanelsummary](./componentsPanel_object/componentsPanel_summary.md)

[componentsPanel.addItemToDocument()](./componentsPanel_object/componentsPanel.md)

[componentsPanel.reload()](./componentsPanel_object/componentsPane1.md)


## contourObject

[Contour Summary](./Contour_object/contour_summary.md)

[contour.fill](./Contour_object/contour.md)

[contour.getHalfEdge()](./Contour_object/contour1.md)

[contour.interior](./Contour_object/contour2.md)

[contour.orientation](./Contour_object/contour3.md)


## documentObject

[documentsummary](./Document_object/document_summary.md)

[document.accName](./Document_object/document.md)

[document.addDataToDocument()](./Document_object/documen1.md)

[document.addDataToSelection()](./Document_object/documen2.md)

[document.addFilter()](./Document_object/documen3.md)

[document.addItem()](./Document_object/documen4.md)

[document.addNewLine()](./Document_object/documen5.md)

[document.addNewOval()](./Document_object/documen6.md)

[document.addNewPrimitiveOval()](./Document_object/documen7.md)

[document.addNewPrimitiveRectangle()](./Document_object/documen8.md)

[document.addNewPublishProfile()](./Document_object/documen9.md)

[document.addNewRectangle()](./Document_object/docume10.md)

[document.addNewScene()](./Document_object/docume11.md)

[document.addNewText()](./Document_object/docume12.md)

[document.addTaggedSwatch()](./Document_object/docu6058.md)

[document.addTaggedSwatchWithColor()](./Document_object/docu6059.md)

[document.align()](./Document_object/docume13.md)

[document.allowScreens.md)-dropped](./Document_object/docume14.md)

[document.arrange()](./Document_object/docume15.md)

[document.as3AutoDeclare](./Document_object/docume16.md)

[document.as3Dialect](./Document_object/docume17.md)

[document.as3ExportFrame](./Document_object/docume18.md)

[document.as3StrictMode](./Document_object/docume19.md)

[document.as3WarningsMode](./Document_object/docume20.md)

[document.asVersion](./Document_object/docume21.md)

[document.autoLabel](./Document_object/docume22.md)

[document.backgroundColor](./Document_object/docume23.md)

[document.breakApart()](./Document_object/docume24.md)

[document.canEditSymbol()](./Document_object/docume25.md)

[document.canRevert()](./Document_object/docume26.md)

[document.canTestMovie()](./Document_object/docume27.md)

[document.canTestScene()](./Document_object/docume28.md)

[document.changeFilterOrder()](./Document_object/docume29.md)

[document.clipCopy()](./Document_object/docume30.md)

[document.clipCut()](./Document_object/docume31.md)

[document.clipPaste()](./Document_object/docume32.md)

[document.close()](./Document_object/docume33.md)

[document.convertLinesToFills()](./Document_object/docume34.md)

[document.convertSelectionToBitmap()](./Document_object/docume35.md)

[document.convertToDoc()](./Document_object/docu6069.md)

[document.convertToSymbol()](./Document_object/docume36.md)

[document.crop()](./Document_object/docume37.md)

[document.currentPublishProfile](./Document_object/docume38.md)

[document.currentTimeline](./Document_object/docume39.md)

[document.Document_object](./Document_object/docume40.md)

[document.deleteEnvelope()](./Document_object/docume41.md)

[document.deletePublishProfile()](./Document_object/docume42.md)

[document.deleteScene()](./Document_object/docume43.md)

[document.deleteSelection()](./Document_object/docume44.md)

[document.deleteTaggedSwatchAtIndex()](./Document_object/docu6065.md)


[document.deleteTaggedSwatchByName()](./Document_object/docu6066.md)

[document.description](./Document_object/docume45.md)

[document.disableAllFilters()](./Document_object/docume46.md)

[document.disableFilter()](./Document_object/docume47.md)

[document.disableOtherFilters()](./Document_object/docume48.md)

[document.distribute()](./Document_object/docume49.md)

[document.distributeToKeyframes()](./Document_object/docume50.md)

[document.distributeToLayers()](./Document_object/docume51.md)

[document.docClass](./Document_object/docume52.md)

[document.documentHasData()](./Document_object/docume53.md)

[document.duplicatePublishProfile()](./Document_object/docume54.md)

[document.duplicateScene()](./Document_object/docume55.md)

[document.duplicateSelection()](./Document_object/docume56.md)

[document.editScene()](./Document_object/docume57.md)

[document.enableAllFilters()](./Document_object/docume58.md)

[document.enableFilter()](./Document_object/docume59.md)

[document.enterEditMode()](./Document_object/docume60.md)

[document.exitEditMode()](./Document_object/docume61.md)

[document.exportCanvasPublishTemplate()](./Document_object/docu6070.md)

[document.exportInstanceToLibrary()](./Document_object/docume62.md)

[document.exportInstanceToPNGSequence()](./Document_object/docume63.md)

[document.exportMedia()](./Document_object/docu6072.md)

[document.exportPNG()](./Document_object/docume64.md)

[document.exportPublishProfile()](./Document_object/docume65.md)

[document.exportPublishProfileString()](./Document_object/docume66.md)

[document.exportSVG()](./Document_object/docu6074.md)

[document.exportSWF()](./Document_object/docume67.md)

[document.exportVideo()](./Document_object/docume68.md)

[document.externalLibraryPath](./Document_object/docume69.md)

[document.forceSimple](./Document_object/docume70.md)

[document.frameRate](./Document_object/docume71.md)

[document.getAlignToDocument()](./Document_object/docume72.md)

[document.getBlendMode()](./Document_object/docume73.md)

[document.getCustomFill()](./Document_object/docume74.md)

[document.getCustomStroke()](./Document_object/docume75.md)

[document.getDataFromDocument()](./Document_object/docume76.md)

[document.getElementProperty()](./Document_object/docume77.md)

[document.getElementTextAttr()](./Document_object/docume78.md)

[document.getFilters()](./Document_object/docume79.md)

[document.getIndexForTaggedSwatchesPalette()](./Document_object/docu6060.md)

[document.getMetadata()](./Document_object/docume80.md)

[document.getMobileSettings()](./Document_object/docume81.md)

[document.getPlayerVersion()](./Document_object/docume82.md)

[document.getPublishDocumentData()](./Document_object/docume83.md)

[document.getSelectionRect()](./Document_object/docume84.md)

[document.getSWFPathFromProfile()](./Document_object/docume85.md)

[document.getTaggedSwatchAtIndex()](./Document_object/docu6061.md)


[document.getTaggedSwatchByName()](./Document_object/docu6062.md)


[document.getTaggedSwatches()](./Document_object/docu6064.md)


[document.getTaggedSwatchesPaletteList()](./Document_object/docu6063.md)

[document.getTelemetryForSwf()](./Document_object/docume86.md)

[document.getTextString()](./Document_object/docume87.md)

[document.getTimeline()](./Document_object/docume88.md)

[document.getTransformationPoint()](./Document_object/docume89.md)

[document.group()](./Document_object/docume90.md)

[document.height](./Document_object/docume91.md)

[document.id](./Document_object/docume92.md)

[document.importCanvasPublishTemplate()](./Document_object/docu6071.md)

[document.importFile()](./Document_object/docume93.md)

[document.importPublishProfile()](./Document_object/docume94.md)

[document.importPublishProfileString()](./Document_object/docume95.md)

[document.importSWF.md)-dropped](./Document_object/docume96.md)

[document.intersect()](./Document_object/docume97.md)

[document.library](./Document_object/docume98.md)

[document.libraryPath](./Document_object/docume99.md)

[document.livePreview](./Document_object/docum100.md)

[document.loadCuepointXML.md)-dropped](./Document_object/docum110.md)

[document.match()](./Document_object/docum120.md)

[document.mouseClick()](./Document_object/docum130.md)

[document.mouseDblClk()](./Document_object/docum140.md)

[document.moveSelectedBezierPointsBy()](./Document_object/docum150.md)

[document.moveSelectionBy()](./Document_object/docum160.md)

[document.optimizeCurves()](./Document_object/docum170.md)

[document.optimizeCurves()](./Document_object/docum180.md)

[document.path](./Document_object/docum190.md)

[document.pathURI](./Document_object/docum200.md)

[document.publish()](./Document_object/docum210.md)

[document.publishProfiles](./Document_object/docum220.md)

[document.punch()](./Document_object/docum230.md)

[document.removeAllFilters()](./Document_object/docum240.md)

[document.removeDataFromDocument()](./Document_object/docum250.md)

[document.removeDataFromSelection()](./Document_object/docum260.md)

[document.removeFilter()](./Document_object/docum270.md)

[document.renamePublishProfile()](./Document_object/docum280.md)

[document.renameScene()](./Document_object/docum290.md)

[document.reorderScene()](./Document_object/docum300.md)

[document.resetOvalObject()](./Document_object/docum310.md)

[document.resetRectangleObject()](./Document_object/docum320.md)

[document.resetTransformation()](./Document_object/docum330.md)

[document.revert()](./Document_object/docum340.md)

[document.rotate3DSelection()](./Document_object/docum350.md)

[document.rotateSelection()](./Document_object/docum360.md)

[document.save()](./Document_object/docum370.md)

[document.saveAndCompact.md)-dropped](./Document_object/docum380.md)

[document.saveAsCopy()](./Document_object/docum390.md)

[document.scaleSelection()](./Document_object/docum400.md)

[document.screenOutline-dropped](./Document_object/docum410.md)

[document.selectAll()](./Document_object/docum420.md)

[document.selection](./Document_object/docum430.md)

[document.selectNone()](./Document_object/docum440.md)

[document.setAlignToDocument()](./Document_object/docum450.md)

[document.setBlendMode()](./Document_object/docum460.md)

[document.setCustomFill()](./Document_object/docum470.md)

[document.setCustomStroke()](./Document_object/docum480.md)

[document.setElementProperty()](./Document_object/docum490.md)

[document.setElementTextAttr()](./Document_object/docum500.md)

[document.setFillColor()](./Document_object/docum510.md)

[document.setFilterProperty()](./Document_object/docum520.md)

[document.setFilters()](./Document_object/docum530.md)

[document.setInstanceAlpha()](./Document_object/docum540.md)

[document.setInstanceBrightness()](./Document_object/docum550.md)

[document.setInstanceTint()](./Document_object/docum560.md)

[document.setMetadata()](./Document_object/docum570.md)

[document.setMobileSettings()](./Document_object/docum580.md)

[document.setOvalObjectProperty()](./Document_object/docum590.md)

[document.setPlayerVersion()](./Document_object/docum600.md)

[document.setPublishDocumentData()](./Document_object/docu9627.md)

[document.setRectangleObjectProperty()](./Document_object/docu9643.md)

[document.setSelectionBounds()](./Document_object/docu9658.md)

[document.setSelectionRect()](./Document_object/docu9689.md)

[document.setStageVanishingPoint()](./Document_object/docu9705.md)

[document.setStageViewAngle()](./Document_object/docu9721.md)

[document.setStroke()](./Document_object/docu9752.md)

[document.setStrokeColor()](./Document_object/docu9768.md)

[document.setStrokeSize()](./Document_object/docu9799.md)

[document.setStrokeStyle()](./Document_object/docu9814.md)

[document.setTaggedSwatchAtIndex()](./Document_object/docu6067.md)

[document.setTaggedSwatchByName()](./Document_object/docu6068.md)

[document.setTextRectangle()](./Document_object/docu9846.md)

[document.setTextSelection()](./Document_object/docu9861.md)

[document.setTextString()](./Document_object/docu9908.md)

[document.setTransformationPoint()](./Document_object/docu9939.md)

[document.silent](./Document_object/docu9971.md)

[document.skewSelection()](./Document_object/docum5.md)

[document.smoothSelection()](./Document_object/docum21.md)

[document.sourcePath](./Document_object/docum36.md)

[document.space()](./Document_object/docum67.md)

[document.straightenSelection()](./Document_object/docum83.md)

[document.swapElement()](./Document_object/docum114.md)

[document.swapStrokeAndFill()](./Document_object/docu5901.md)

[document.swfJPEGQuality](./Document_object/docu5932.md)

[document.testMovie()](./Document_object/docu5948.md)

[document.testScene()](./Document_object/docu5979.md)

[document.timelines](./Document_object/docu5995.md)

[document.traceBitmap()](./Document_object/docu6010.md)

[document.translate3DCenter()](./Document_object/docu6042.md)

[document.translate3DSelection()](./Document_object/docu6057.md)

[document.transformSelection()](./Document_object/docu6073.md)

[document.unGroup()](./Document_object/docu6104.md)

[document.union()](./Document_object/docu6120.md)

[document.unlockAllElements()](./Document_object/docu6135.md)

[document.viewMatrix](./Document_object/docu6167.md)

[document.width](./Document_object/docu6182.md)

[document.xmlPanel()](./Document_object/docu6198.md)

[document.zoomFactor](./Document_object/docu6229.md)



## drawingLayer

[drawingLayersummary](./drawingLayer_object/drawingLayersummary.md)

[drawingLayer.beginDraw()](./drawingLayer_object/drawingLayer.md)

[drawingLayer.beginFrame()](./drawingLayer_object/drawingLaye1.md)

[drawingLayer.cubicCurveTo()](./drawingLayer_object/drawingLaye2.md)

[drawingLayer.curveTo()](./drawingLayer_object/drawingLaye3.md)

[drawingLayer.drawPath()](./drawingLayer_object/drawingLaye4.md)

[drawingLayer.endDraw()](./drawingLayer_object/drawingLaye5.md)

[drawingLayer.endFrame()](./drawingLayer_object/drawingLaye6.md)

[drawingLayer.lineTo()](./drawingLayer_object/drawingLaye7.md)

[drawingLayer.moveTo()](./drawingLayer_object/drawingLaye8.md)

[drawingLayer.newPath()](./drawingLayer_object/drawingLaye9.md)

[drawingLayer.setColor()](./drawingLayer_object/drawingLay10.md)

[drawingLayer.setFill()](./drawingLayer_object/drawingLay11.md)

[drawingLayer.setStroke()](./drawingLayer_object/drawingLay12.md)

## edgeObject

[edgesummary](./Edge_object/edge_summary.md)

[edge.cubicSegmentIndex](./Edge_object/edge.md)

[edge.getControl()](./Edge_object/edge1.md)

[edge.getHalfEdge()](./Edge_object/edge2.md)

[edge.id](./Edge_object/edge3.md)

[edge.isLine](./Edge_object/edge4.md)

[edge.setControl()](./Edge_object/edge5.md)

[edge.splitEdge()](./Edge_object/edge6.md)

[edge.stroke](./Edge_object/edge7.md)


## elementObject

[element.depth](./Element_object/element.md)

[element.elementType](./Element_object/element1.md)

[element.getPersistentData()](./Element_object/element2.md)

[element.getPublishPersistentData()](./Element_object/element3.md)

[element.getTransformationPoint()](./Element_object/element4.md)

[element.hasPersistentData()](./Element_object/element5.md)

[element.height](./Element_object/element6.md)

[element.layer](./Element_object/element7.md)

[element.left](./Element_object/element8.md)

[element.locked](./Element_object/element9.md)

[element.matrix](./Element_object/elemen10.md)

[element.name](./Element_object/elemen11.md)

[element.removePersistentData()](./Element_object/elemen12.md)

[element.rotation](./Element_object/elemen13.md)

[element.scaleX](./Element_object/elemen14.md)

[element.scaleY](./Element_object/elemen15.md)

[element.selected](./Element_object/elemen16.md)

[element.setPersistentData()](./Element_object/elemen17.md)

[element.setPublishPersistentData()](./Element_object/elemen18.md)

[element.setTransformationPoint()](./Element_object/elemen19.md)

[element.skewX](./Element_object/elemen20.md)

[element.skewY](./Element_object/elemen21.md)

[element.top](./Element_object/elemen22.md)

[element.transformX](./Element_object/elemen23.md)

[element.transformY](./Element_object/elemen24.md)

[element.width](./Element_object/elemen25.md)

[element.x](./Element_object/elemen26.md)

[element.y](./Element_object/elemen27.md)


## fillObject

[fillsummary](./Fill_object/fill_summary.md)

[fill.bitmapIsClipped](./Fill_object/fill.md)

[fill.bitmapPath](./Fill_object/fill1.md)

[fill.color](./Fill_object/fill2.md)

[fill.colorArray](./Fill_object/fill3.md)

[fill.focalPoint](./Fill_object/fill4.md)

[fill.linearRGB](./Fill_object/fill5.md)

[fill.matrix](./Fill_object/fill6.md)

[fill.overflow](./Fill_object/fill7.md)

[fill.posArray](./Fill_object/fill8.md)

[fill.style](./Fill_object/fill9.md)


## filterObject

[filtersummary](./Filter_object/filter_summary.md)

[filter.angle](./Filter_object/filter.md)

[filter.blurX](./Filter_object/filter1.md)

[filter.blurY](./Filter_object/filter2.md)

[filter.brightness](./Filter_object/filter3.md)

[filter.color](./Filter_object/filter4.md)

[filter.contrast](./Filter_object/filter5.md)

[filter.distance](./Filter_object/filter6.md)

[filter.enabled](./Filter_object/filter7.md)

[filter.hideObject](./Filter_object/filter8.md)

[filter.highlightColor](./Filter_object/filter9.md)

[filter.hue](./Filter_object/filter10.md)

[filter.inner](./Filter_object/filter11.md)

[filter.knockout](./Filter_object/filter12.md)

[filter.name](./Filter_object/filter13.md)

[filter.quality](./Filter_object/filter14.md)

[filter.saturation](./Filter_object/filter15.md)

[filter.shadowColor](./Filter_object/filter16.md)

[filter.strength](./Filter_object/filter17.md)

[filter.type](./Filter_object/filter18.md)


## flash(fl.())Object

[flsummary](./flash_object_(fl)/fl_summary.md)

[fl.actionsPanel](./flash_object_(fl)/fl.md)

[fl.addEventListener()](./flash_object_(fl)/fl1.md)

[fl.addToolInToolbar()](./flash_object_(fl)/fl82.md)

[fl.as3PackagePaths](./flash_object_(fl)/fl2.md)

[fl.browseForFileURL()](./flash_object_(fl)/fl3.md)

[fl.browseForFolderURL()](./flash_object_(fl)/fl4.md)

[fl.clearPublishCache()](./flash_object_(fl)/fl5.md)

[fl.clipCopyString()](./flash_object_(fl)/fl6.md)

[fl.closeAll()](./flash_object_(fl)/fl7.md)

[fl.closeAllPlayerDocuments()](./flash_object_(fl)/fl8.md)

[fl.closeDocument()](./flash_object_(fl)/fl9.md)

[fl.compilerErrors](./flash_object_(fl)/fl10.md)

[fl.componentsPanel](./flash_object_(fl)/fl11.md)

[fl.configDirectory](./flash_object_(fl)/fl12.md)

[fl.configURI](./flash_object_(fl)/fl13.md)

[fl.contactSensitiveSelection](./flash_object_(fl)/fl14.md)

[fl.copyLibraryItem()](./flash_object_(fl)/fl15.md)

[fl.createDocument()](./flash_object_(fl)/fl16.md)

[fl.createNewDocList](./flash_object_(fl)/fl17.md)

[fl.createNewDocListType](./flash_object_(fl)/fl18.md)

[fl.createNewTemplateList](./flash_object_(fl)/fl19.md)

[fl.documents](./flash_object_(fl)/fl20.md)

[fl.drawingLayer](./flash_object_(fl)/fl21.md)

[fl.exportPublishProfileString()](./flash_object_(fl)/fl22.md)

[fl.externalLibraryPath](./flash_object_(fl)/fl23.md)

[fl.fileExists()](./flash_object_(fl)/fl24.md)

[fl.findDocumentDOM()](./flash_object_(fl)/fl25.md)

[fl.findDocumentIndex()](./flash_object_(fl)/fl26.md)

[fl.findObjectInDocByName()](./flash_object_(fl)/fl27.md)

[fl.findObjectInDocByType()](./flash_object_(fl)/fl28.md)

[fl.flexSDKPath](./flash_object_(fl)/fl29.md)

[fl.getAppMemoryInfo()](./flash_object_(fl)/fl30.md)

[fl.getDocumentDOM()](./flash_object_(fl)/fl31.md)

[fl.getThemeColor()](./flash_object_(fl)/fl32.md)

[fl.getThemeColorParameters()](./flash_object_(fl)/fl33.md)

[fl.getThemeFontInfo()](./flash_object_(fl)/fl34.md)

[fl.getSwfPanel()](./flash_object_(fl)/fl35.md)

[fl.installedPlayers](./flash_object_(fl)/fl36.md)

[fl.isFontInstalled()](./flash_object_(fl)/fl37.md)

[fl.languageCode](./flash_object_(fl)/fl38.md)

[fl.libraryPath](./flash_object_(fl)/fl39.md)

[fl.mapPlayerURL()](./flash_object_(fl)/fl40.md)

[fl.Math](./flash_object_(fl)/fl41.md)

[fl.mruRecentFileList](./flash_object_(fl)/fl42.md)

[fl.mruRecentFileListType](./flash_object_(fl)/fl43.md)

[fl.objectDrawingMode](./flash_object_(fl)/fl44.md)

[fl.openDocument()](./flash_object_(fl)/fl45.md)

[fl.openScript()](./flash_object_(fl)/fl46.md)

[fl.outputPanel](./flash_object_(fl)/fl47.md)

[fl.packagePaths-dropped](./flash_object_(fl)/fl48.md)

[fl.presetPanel](./flash_object_(fl)/fl49.md)

[fl.publishCacheDiskSizeMax](./flash_object_(fl)/fl50.md)

[fl.publishCacheEnabled](./flash_object_(fl)/fl51.md)

[fl.publishCacheMemoryEntrySizeLimit](./flash_object_(fl)/fl52.md)

[fl.publishCacheMemorySizeMax](./flash_object_(fl)/fl53.md)

[fl.publishDocument()](./flash_object_(fl)/fl54.md)

[fl.quit()](./flash_object_(fl)/fl55.md)

[fl.reloadEffects.md)-dropped](./flash_object_(fl)/fl56.md)

[fl.reloadTools()](./flash_object_(fl)/fl57.md)

[fl.removeEventListener()](./flash_object_(fl)/fl58.md)

[fl.resetAS3PackagePaths()](./flash_object_(fl)/fl59.md)

[fl.resetPackagePaths.md)-dropped](./flash_object_(fl)/fl60.md)

[fl.revertDocument()](./flash_object_(fl)/fl61.md)

[fl.runScript()](./flash_object_(fl)/fl62.md)

[fl.saveAll()](./flash_object_(fl)/fl63.md)

[fl.saveDocument()](./flash_object_(fl)/fl64.md)

[fl.saveDocumentAs()](./flash_object_(fl)/fl65.md)

[fl.scriptURI](./flash_object_(fl)/fl66.md)

[fl.selectElement()](./flash_object_(fl)/fl67.md)

[fl.selectTool()](./flash_object_(fl)/fl68.md)

[fl.setActiveWindow()](./flash_object_(fl)/fl69.md)

[fl.showIdleMessage()](./flash_object_(fl)/fl70.md)

[fl.setPrefBoolean()](./flash_object_(fl)/fl71.md)

[fl.sourcePath](./flash_object_(fl)/fl72.md)

[fl.spriteSheetExporter](./flash_object_(fl)/fl73.md)

[fl.swfPanels](./flash_object_(fl)/fl74.md)

[fl.toggleBreakpoint()](./flash_object_(fl)/fl75.md)

[fl.tools](./flash_object_(fl)/fl76.md)

[fl.trace()](./flash_object_(fl)/fl77.md)

[fl.version](./flash_object_(fl)/fl78.md)

[fl.xmlPanel()](./flash_object_(fl)/fl79.md)

[fl.xmlPanelFromString()](./flash_object_(fl)/fl80.md)

[fl.xmlui](./flash_object_(fl)/fl81.md)


## FLfileObject

[FLfilesummary](./FLfile_object/FLfile_summary.md)

[FLfile.copy()](./FLfile_object/FLfile.md)

[FLfile.createFolder()](./FLfile_object/FLfile1.md)

[FLfile.exists()](./FLfile_object/FLfile2.md)

[FLfile.getAttributes()](./FLfile_object/FLfile3.md)

[FLfile.getCreationDate()](./FLfile_object/FLfile4.md)

[FLfile.getCreationDateObj()](./FLfile_object/FLfile5.md)

[FLfile.getModificationDate()](./FLfile_object/FLfile6.md)

[FLfile.getModificationDateObj()](./FLfile_object/FLfile7.md)

[FLfile.getSize()](./FLfile_object/FLfile8.md)

[FLfile.listFolder()](./FLfile_object/FLfile9.md)

[FLfile.platformPathToURI()](./FLfile_object/FLfile10.md)

[FLfile.read()](./FLfile_object/FLfile11.md)

[FLfile.remove()](./FLfile_object/FLfile12.md)

[FLfile.setAttributes()](./FLfile_object/FLfile13.md)

[FLfile.uriToPlatformPath()](./FLfile_object/FLfile14.md)

[FLfile.write()](./FLfile_object/FLfile15.md)


## folderItemObject

[folderItemsummary](./folderItem_object/folderItem_summary.md)


## fontItemObject

[fontItemsummary](./fontItem_object/fontItem_summary.md)

[fontItem.bitmap](./fontItem_object/fontItem.md)

[fontItem.bold](./fontItem_object/fontIte1.md)

[fontItem.embeddedCharacters](./fontItem_object/fontIte2.md)

[fontItem.embedRanges](./fontItem_object/fontIte3.md)

[fontItem.embedVariantGlyphs](./fontItem_object/fontIte4.md)

[fontItem.font](./fontItem_object/fontIte5.md)

[fontItem.isDefineFont4Symbol](./fontItem_object/fontIte6.md)

[fontItem.italic](./fontItem_object/fontIte7.md)

[fontItem.size](./fontItem_object/fontIte8.md)


## FrameObject

[framesummary](./Frame_object/frame_summary.md)

[frame.convertMotionObjectTo2D()](./Frame_object/frame.md)

[frame.convertMotionObjectTo3D()](./Frame_object/frame1.md)

[frame.convertToFrameByFrameAnimation()](./Frame_object/frame2.md)

[frame.actionScript](./Frame_object/frame3.md)

[frame.duration](./Frame_object/frame4.md)

[frame.elements](./Frame_object/frame5.md)

[frame.getCustomEase()](./Frame_object/frame6.md)

[frame.getMotionObjectXML()](./Frame_object/frame7.md)

[frame.getSoundEnvelope()](./Frame_object/frame8.md)

[frame.getSoundEnvelopeLimits()](./Frame_object/frame9.md)

[frame.hasCustomEase](./Frame_object/frame10.md)

[frame.hasMotionPath()](./Frame_object/frame11.md)

[frame.is3DMotionObject()](./Frame_object/frame12.md)

[frame.isEmpty()](./Frame_object/frame13.md)

[frame.isMotionObject()](./Frame_object/frame14.md)

[frame.labelType](./Frame_object/frame15.md)

[frame.motionTweenOrientToPath](./Frame_object/frame16.md)

[frame.motionTweenRotate](./Frame_object/frame17.md)

[frame.motionTweenRotateTimes](./Frame_object/frame18.md)

[frame.motionTweenScale](./Frame_object/frame19.md)

[frame.motionTweenSnap](./Frame_object/frame20.md)

[frame.motionTweenSync](./Frame_object/frame21.md)

[frame.name](./Frame_object/frame22.md)

[frame.selectMotionPath()](./Frame_object/frame23.md)

[frame.setCustomEase()](./Frame_object/frame24.md)

[frame.setMotionObjectDuration()](./Frame_object/frame25.md)

[frame.setMotionObjectXML()](./Frame_object/frame26.md)

[frame.setSoundEnvelope()](./Frame_object/frame27.md)

[frame.setSoundEnvelopeLimits()](./Frame_object/frame28.md)

[frame.shapeTweenBlend](./Frame_object/frame29.md)

[frame.soundEffect](./Frame_object/frame30.md)

[frame.soundLibraryItem](./Frame_object/frame31.md)

[frame.soundLoop](./Frame_object/frame32.md)

[frame.soundLoopMode](./Frame_object/frame33.md)

[frame.soundName](./Frame_object/frame34.md)

[frame.soundSync](./Frame_object/frame35.md)

[frame.startFrame](./Frame_object/frame36.md)

[frame.tweenEasing](./Frame_object/frame37.md)

[frame.tweenInstanceName](./Frame_object/frame38.md)

[frame.tweenType](./Frame_object/frame39.md)

[frame.useSingleEaseCurve](./Frame_object/frame40.md)


## HalfEdgeObject

[halfEdgesummary](./HalfEdge_object/halfEdge_summary.md)

[halfEdge.getEdge()](./HalfEdge_object/halfEdge.md)

[halfEdge.getNext()](./HalfEdge_object/halfEdg1.md)

[halfEdge.getOppositeHalfEdge()](./HalfEdge_object/halfEdg2.md)

[halfEdge.getPrev()](./HalfEdge_object/halfEdg3.md)

[halfEdge.getVertex()](./HalfEdge_object/halfEdg4.md)

[halfEdge.id](./HalfEdge_object/halfEdg5.md)


## InstanceObject

[instancesummary](./Instance_object/instance_summary.md)

[instance.instanceType](./Instance_object/instance.md)

[instance.libraryItem](./Instance_object/instanc1.md)


## ItemObject

[itemsummary](./Item_object/item_summary.md)

[item.addData()](./Item_object/item.md)

[item.getData()](./Item_object/item1.md)

[item.getPublishData()](./Item_object/item2.md)

[item.hasData()](./Item_object/item3.md)

[item.itemType](./Item_object/item4.md)

[item.linkageBaseClass](./Item_object/item5.md)

[item.linkageClassName](./Item_object/item6.md)

[item.linkageExportForAS](./Item_object/item7.md)

[item.linkageExportForRS](./Item_object/item8.md)

[item.linkageExportInFirstFrame](./Item_object/item9.md)

[item.linkageIdentifier](./Item_object/item10.md)

[item.linkageImportForRS](./Item_object/item11.md)

[item.linkageURL](./Item_object/item12.md)

[item.name](./Item_object/item13.md)

[item.removeData()](./Item_object/item14.md)

[item.setPublishData()](./Item_object/item15.md)


## LayerObject

[layersummary](./Layer_object/layer_summary.md)

[layer.animationType](./Layer_object/layer.md)

[layer.color](./Layer_object/layer1.md)

[layer.frameCount](./Layer_object/layer2.md)

[layer.frames](./Layer_object/layer3.md)

[layer.getBlendModeAtFrame()](./Layer_object/layer13.md)

[layer.getColorTransformAtFrame()](./Layer_object/layer14.md)

[layer.getFiltersAtFrame()](./Layer_object/layer15.md)

[layer.getZDepthAtFrame()](./Layer_object/layer11.md)

[layer.height](./Layer_object/layer4.md)

[layer.layerType](./Layer_object/layer5.md)

[layer.locked](./Layer_object/layer6.md)

[layer.name](./Layer_object/layer7.md)

[layer.outline](./Layer_object/layer8.md)

[layer.parentLayer](./Layer_object/layer9.md)

[layer.setBlendModeAtFrame()](./Layer_object/layer16.md)

[layer.setColorTransformAtFrame()](./Layer_object/layer17.md)

[layer.setFiltersAtFrame()](./Layer_object/layer18.md)

[layer.setZDepthAtFrame()](./Layer_object/layer12.md)

[layer.visible](./Layer_object/layer10.md)

    
## LayerParentingObject

[layerParentingsummary](./Layer_Parenting_Object/layerParenting_summary.md)

[layer.getRigMatrixAtFrame()](./Layer_Parenting_Object/layerParenting3.md)

[layer.getRigParentAtFrame()](./Layer_Parenting_Object/layerParenting1.md)

[layer.setRigParentAtFrame()](./Layer_Parenting_Object/layerParenting2.md)


## libraryObject

[librarysummary](./library_object/library_summary.md)

[library.addItemToDocument()](./library_object/library.md)

[library.addNewItem()](./library_object/library1.md)

[library.deleteItem()](./library_object/library2.md)

[library.duplicateItem()](./library_object/library3.md)

[library.editItem()](./library_object/library4.md)

[library.findItemIndex()](./library_object/library5.md)

[library.getItemProperty()](./library_object/library6.md)

[library.getItemType()](./library_object/library7.md)

[library.getSelectedItems()](./library_object/library8.md)

[library.itemExists()](./library_object/library9.md)

[library.items](./library_object/librar10.md)

[library.moveToFolder()](./library_object/librar11.md)

[library.newFolder()](./library_object/librar12.md)

[library.renameItem()](./library_object/librar13.md)

[library.selectAll()](./library_object/librar14.md)

[library.selectItem()](./library_object/librar15.md)

[library.selectNone()](./library_object/librar16.md)

[library.setItemProperty()](./library_object/librar17.md)

[library.unusedItems](./library_object/librar18.md)

[library.updateItem()](./library_object/librar19.md)


## MathObject

[Mathsummary](./Math_object/Math_summary.md)

[Math.concatMatrix()](./Math_object/Math.md)

[Math.invertMatrix()](./Math_object/Math1.md)

[Math.pointDistance()](./Math_object/Math2.md)

[Math.transformPoint()](./Math_object/Math3.md)


## MatrixObject

[matrixsummary](./Matrix_object/matrix_summary.md)

[matrix.a](./Matrix_object/matrix.md)

[matrix.b](./Matrix_object/matrix1.md)

[matrix.c](./Matrix_object/matrix2.md)

[matrix.d](./Matrix_object/matrix3.md)

[matrix.tx](./Matrix_object/matrix4.md)

[matrix.ty](./Matrix_object/matrix5.md)


## outputPanelObject

[outputPanelsummary](./outputPanel_object/outputPanel_summary.md)

[outputPanel.clear()](./outputPanel_object/outputPanel.md)

[outputPanel.save()](./outputPanel_object/outputPane1.md)

[outputPanel.trace()](./outputPanel_object/outputPane2.md)


## OvalObject

[OvalObjectsummary](./Oval_object/OvalObject_summary.md)

[OvalObject.closePath](./Oval_object/OvalObject.md)

[OvalObject.endAngle](./Oval_object/OvalObjec1.md)

[OvalObject.innerRadius](./Oval_object/OvalObjec2.md)

[OvalObject.startAngle](./Oval_object/OvalObjec3.md)


## Parameterobject

[parametersummary](./Parameter_object/parameter_summary.md)

[parameter.category](./Parameter_object/parameter.md)

[parameter.insertItem()](./Parameter_object/paramete1.md)

[parameter.listIndex](./Parameter_object/paramete2.md)

[parameter.name](./Parameter_object/paramete3.md)

[parameter.removeItem()](./Parameter_object/paramete4.md)

[parameter.value](./Parameter_object/paramete5.md)

[parameter.valueType](./Parameter_object/paramete6.md)

[parameter.verbose](./Parameter_object/paramete7.md)


## Pathobject

[pathsummary](./Path_object/path_summary.md)

[path.addCubicCurve()](./Path_object/path.md)

[path.addCurve()](./Path_object/path1.md)

[path.addPoint()](./Path_object/path2.md)

[path.clear()](./Path_object/path3.md)

[path.close()](./Path_object/path4.md)

[path.makeShape()](./Path_object/path5.md)

[path.newContour()](./Path_object/path6.md)

[path.nPts](./Path_object/path7.md)


## presetItemobject

[presetItemsummary](./presetItem_object/presetItem_summary.md)

[presetItem.isDefault](./presetItem_object/presetItem.md)

[presetItem.isFolder](./presetItem_object/presetIte1.md)

[presetItem.level](./presetItem_object/presetIte2.md)

[presetItem.name](./presetItem_object/presetIte3.md)

[presetItem.open](./presetItem_object/presetIte4.md)

[presetItem.path](./presetItem_object/presetIte5.md)


## presetPanelobject

[presetPanelsummary](./presetPanel_object/presetPanel_summary.md)

[presetPanel.addNewItem()](./presetPanel_object/presetPanel.md)

[presetPanel.applyPreset()](./presetPanel_object/presetPane1.md)

[presetPanel.deleteFolder()](./presetPanel_object/presetPane2.md)

[presetPanel.deleteItem()](./presetPanel_object/presetPane3.md)

[presetPanel.expandFolder()](./presetPanel_object/presetPane4.md)

[presetPanel.exportItem()](./presetPanel_object/presetPane5.md)

[presetPanel.findItemIndex()](./presetPanel_object/presetPane6.md)

[presetPanel.getSelectedItems()](./presetPanel_object/presetPane7.md)

[presetPanel.importItem()](./presetPanel_object/presetPane8.md)

[presetPanel.items](./presetPanel_object/presetPane9.md)

[presetPanel.moveToFolder()](./presetPanel_object/presetPan10.md)

[presetPanel.newFolder()](./presetPanel_object/presetPan11.md)

[presetPanel.renameItem()](./presetPanel_object/presetPan12.md)

[presetPanel.selectItem()](./presetPanel_object/presetPan13.md)


## Rectangleobject

[RectangleObjectsummary](./Rectangle_object/RectangleObject_summary.md)

[RectangleObject.bottomLeftRadius](./Rectangle_object/RectangleObject.md)

[RectangleObject.bottomRightRadius](./Rectangle_object/RectangleObjec1.md)

[RectangleObject.lockFlag](./Rectangle_object/RectangleObjec2.md)

[RectangleObject.topLeftRadius](./Rectangle_object/RectangleObjec3.md)

[RectangleObject.topRightRadius](./Rectangle_object/RectangleObjec4.md)


## Shapeobject

[shapesummary](./Shape_object/shape_summary.md)

[shape.beginEdit()](./Shape_object/shape.md)

[shape.contours](./Shape_object/shape1.md)

[shape.deleteEdge()](./Shape_object/shape2.md)

[shape.edges](./Shape_object/shape3.md)

[shape.endEdit()](./Shape_object/shape4.md)

[shape.getCubicSegmentPoints()](./Shape_object/shape5.md)

[shape.isDrawingObject](./Shape_object/shape6.md)

[shape.isFloating](./Shape_object/shape7.md)

[shape.isGroup](./Shape_object/shape8.md)

[shape.isOvalObject](./Shape_object/shape9.md)

[shape.isRectangleObject](./Shape_object/shape10.md)

[shape.members](./Shape_object/shape11.md)

[shape.numCubicSegments](./Shape_object/shape12.md)

[shape.vertices](./Shape_object/shape13.md)


## SoundItemobject

[soundItemsummary](./SoundItem_object/soundItem_summary.md)

[soundItem.bitRate](./SoundItem_object/soundItem.md)

[soundItem.bits](./SoundItem_object/soundIte1.md)

[soundItem.compressionType](./SoundItem_object/soundIte2.md)

[soundItem.convertStereoToMono](./SoundItem_object/soundIte3.md)

[soundItem.exportToFile()](./SoundItem_object/soundIte4.md)

[soundItem.fileLastModifiedDate](./SoundItem_object/soundIte5.md)

[soundItem.lastModifiedDate](./SoundItem_object/soundIte6.md)

[soundItem.originalCompressionType](./SoundItem_object/soundIte7.md)

[soundItem.quality](./SoundItem_object/soundIte8.md)

[soundItem.sampleRate](./SoundItem_object/soundIte9.md)

[soundItem.sourceFileExists](./SoundItem_object/soundIt10.md)

[soundItem.sourceFileIsCurrent](./SoundItem_object/soundIt11.md)

[soundItem.sourceFilePath](./SoundItem_object/soundIt12.md)

[soundItem.useImportedMP3Quality](./SoundItem_object/soundIt13.md)


## SpriteSheetExporterobject

[SpriteSheetExportersummary](./SpriteSheetExporter_object/SpriteSheetExporter_summary.md)

[SpriteSheetExporter.addBitmap()](./SpriteSheetExporter_object/SpriteSheetExporter.md)

[SpriteSheetExporter.addSymbol()](./SpriteSheetExporter_object/SpriteSheetExporte1.md)

[SpriteSheetExporter.algorithm](./SpriteSheetExporter_object/SpriteSheetExporte2.md)

[SpriteSheetExporter.allowRotate](./SpriteSheetExporter_object/SpriteSheetExporte3.md)

[SpriteSheetExporter.allowTrimming](./SpriteSheetExporter_object/SpriteSheetExporte4.md)

[SpriteSheetExporter.app](./SpriteSheetExporter_object/SpriteSheetExporte5.md)

[SpriteSheetExporter.autoSize](./SpriteSheetExporter_object/SpriteSheetExporte6.md)

[SpriteSheetExporter.beginExport()](./SpriteSheetExporter_object/SpriteSheetExporte7.md)

[SpriteSheetExporter.borderPadding](./SpriteSheetExporter_object/SpriteSheetExporte8.md)

[SpriteSheetExporter.canBorderPad](./SpriteSheetExporter_object/SpriteSheetExporte9.md)

[SpriteSheetExporter.canRotate](./SpriteSheetExporter_object/SpriteSheetExport10.md)

[SpriteSheetExporter.canTrim](./SpriteSheetExporter_object/SpriteSheetExport11.md)

[SpriteSheetExporter.canShapePad](./SpriteSheetExporter_object/SpriteSheetExport12.md)

[SpriteSheetExporter.canStackDuplicateFrames](./SpriteSheetExporter_object/SpriteSheetExport13.md)

[SpriteSheetExporter.changeSymbol()](./SpriteSheetExporter_object/SpriteSheetExport14.md)

[SpriteSheetExporter.exportSpriteSheet()](./SpriteSheetExporter_object/SpriteSheetExport15.md)

[SpriteSheetExporter.format](./SpriteSheetExporter_object/SpriteSheetExport16.md)

[SpriteSheetExporter.image](./SpriteSheetExporter_object/SpriteSheetExport17.md)

[SpriteSheetExporter.layoutFormat](./SpriteSheetExporter_object/SpriteSheetExport18.md)

[SpriteSheetExporter.maxSheetHeight](./SpriteSheetExporter_object/SpriteSheetExport19.md)

[SpriteSheetExporter.maxSheetWidth](./SpriteSheetExporter_object/SpriteSheetExport20.md)

[SpriteSheetExporter.overflowed](./SpriteSheetExporter_object/SpriteSheetExport21.md)

[SpriteSheetExporter.removeBitmap()](./SpriteSheetExporter_object/SpriteSheetExport22.md)

[SpriteSheetExporter.removeSymbol()](./SpriteSheetExporter_object/SpriteSheetExport23.md)

[SpriteSheetExporter.shapePadding](./SpriteSheetExporter_object/SpriteSheetExport24.md)

[SpriteSheetExporter.sheetHeight](./SpriteSheetExporter_object/SpriteSheetExport25.md)

[SpriteSheetExporter.sheetWidth](./SpriteSheetExporter_object/SpriteSheetExport26.md)

[SpriteSheetExporter.stackDuplicateFrames](./SpriteSheetExporter_object/SpriteSheetExport27.md)

[SpriteSheetExporter.version](./SpriteSheetExporter_object/SpriteSheetExport28.md)


## Strokeobject

[strokesummary](./Stroke_object/stroke_summary.md)

[stroke.breakAtCorners](./Stroke_object/stroke.md)

[stroke.capType](./Stroke_object/stroke1.md)

[stroke.color](./Stroke_object/stroke2.md)

[stroke.curve](./Stroke_object/stroke3.md)

[stroke.dash1](./Stroke_object/stroke4.md)

[stroke.dash2](./Stroke_object/stroke5.md)

[stroke.density](./Stroke_object/stroke6.md)

[stroke.dotSize](./Stroke_object/stroke7.md)

[stroke.dotSpace](./Stroke_object/stroke8.md)

[stroke.hatchThickness](./Stroke_object/stroke9.md)

[stroke.jiggle](./Stroke_object/stroke10.md)

[stroke.joinType](./Stroke_object/stroke11.md)

[stroke.length](./Stroke_object/stroke12.md)

[stroke.miterLimit](./Stroke_object/stroke13.md)

[stroke.pattern](./Stroke_object/stroke14.md)

[stroke.rotate](./Stroke_object/stroke15.md)

[stroke.scaleType](./Stroke_object/stroke16.md)

[stroke.shapeFill](./Stroke_object/stroke17.md)

[stroke.space](./Stroke_object/stroke18.md)

[stroke.strokeHinting](./Stroke_object/stroke19.md)

[stroke.style](./Stroke_object/stroke20.md)

[stroke.thickness](./Stroke_object/stroke21.md)

[stroke.variation](./Stroke_object/stroke22.md)

[stroke.waveHeight](./Stroke_object/stroke23.md)

[stroke.waveLength](./Stroke_object/stroke24.md)


## swfPanelobject

[swfPanelsummary](./swfPanel_object/swfPanel_summary.md)

[swfPanel.call()](./swfPanel_object/swfPanel.md)

[swfPanel.dpiScaleFactorX](./swfPanel_object/swfPane1.md)

[swfPanel.dpiScaleFactorY](./swfPanel_object/swfPane2.md)

[swfPanel.name](./swfPanel_object/swfPane3.md)

[swfPanel.path](./swfPanel_object/swfPane4.md)

[swfPanel.reload()](./swfPanel_object/swfPane5.md)

[swfPanel.setFocus()](./swfPanel_object/swfPane6.md)


## SymbolInstanceobject

[symbolInstancesummary](./SymbolInstance_object/symbolInstance_summary.md)

[symbolInstance.accName](./SymbolInstance_object/symbolInstance.md)

[symbolInstance.actionScript-dropped](./SymbolInstance_object/symbolInstanc1.md)

[symbolInstance.backgroundColor](./SymbolInstance_object/symbolInstanc2.md)

[symbolInstance.bitmapRenderMode](./SymbolInstance_object/symbolInstanc3.md)

[symbolInstance.blendMode](./SymbolInstance_object/symbolInstanc4.md)

[symbolInstance.brightness](./SymbolInstance_object/symbolInstanc5.md)

[symbolInstance.buttonTracking](./SymbolInstance_object/symbolInstanc6.md)

[symbolInstance.cacheAsBitmap](./SymbolInstance_object/symbolInstanc7.md)

[symbolInstance.colorAlphaAmount](./SymbolInstance_object/symbolInstanc8.md)

[symbolInstance.colorAlphaPercent](./SymbolInstance_object/symbolInstanc9.md)

[symbolInstance.colorBlueAmount](./SymbolInstance_object/symbolInstan10.md)

[symbolInstance.colorBluePercent](./SymbolInstance_object/symbolInstan11.md)

[symbolInstance.colorGreenAmount](./SymbolInstance_object/symbolInstan12.md)

[symbolInstance.colorGreenPercent](./SymbolInstance_object/symbolInstan13.md)

[symbolInstance.colorMode](./SymbolInstance_object/symbolInstan14.md)

[symbolInstance.colorRedAmount](./SymbolInstance_object/symbolInstan15.md)

[symbolInstance.colorRedPercent](./SymbolInstance_object/symbolInstan16.md)

[symbolInstance.description](./SymbolInstance_object/symbolInstan17.md)

[symbolInstance.filters](./SymbolInstance_object/symbolInstan18.md)

[symbolInstance.firstFrame](./SymbolInstance_object/symbolInstan19.md)

[symbolInstance.forceSimple](./SymbolInstance_object/symbolInstan20.md)

[symbolInstance.is3D](./SymbolInstance_object/symbolInstan21.md)

[symbolInstance.loop](./SymbolInstance_object/symbolInstan22.md)

[symbolInstance.shortcut](./SymbolInstance_object/symbolInstan23.md)

[symbolInstance.silent](./SymbolInstance_object/symbolInstan24.md)

[symbolInstance.symbolType](./SymbolInstance_object/symbolInstan25.md)

[symbolInstance.tabIndex](./SymbolInstance_object/symbolInstan26.md)

[symbolInstance.tintColor](./SymbolInstance_object/symbolInstan27.md)

[symbolInstance.tintPercent](./SymbolInstance_object/symbolInstan28.md)

[symbolInstance.useBackgroundColor](./SymbolInstance_object/symbolInstan29.md)

[symbolInstance.visible](./SymbolInstance_object/symbolInstan30.md)


## SymbolItemobject

[symbolItemsummary](./SymbolItem_object/symbolItem_summary.md)

[symbolItem.convertToCompiledClip()](./SymbolItem_object/symbolItem.md)

[symbolItem.exportSWC()](./SymbolItem_object/symbolIte1.md)

[symbolItem.exportSWF()](./SymbolItem_object/symbolIte2.md)

[symbolItem.exportToLibrary()](./SymbolItem_object/symbolIte3.md)

[symbolItem.exportToPNGSequence()](./SymbolItem_object/symbolIte4.md)

[symbolItem.lastModifiedDate](./SymbolItem_object/symbolIte5.md)

[symbolItem.scalingGrid](./SymbolItem_object/symbolIte6.md)

[symbolItem.scalingGridRect](./SymbolItem_object/symbolIte7.md)

[symbolItem.sourceAutoUpdate](./SymbolItem_object/symbolIte8.md)

[symbolItem.sourceFilePath](./SymbolItem_object/symbolIte9.md)

[symbolItem.sourceLibraryName](./SymbolItem_object/symbolIt10.md)

[symbolItem.symbolType](./SymbolItem_object/symbolIt11.md)

[symbolItem.timeline](./SymbolItem_object/symbolIt12.md)


## TextObject

[textsummary](./Text_object/text_summary.md)

[text.accName](./Text_object/text.md)

[text.antiAliasSharpness](./Text_object/text1.md)

[text.antiAliasThickness](./Text_object/text2.md)

[text.autoExpand](./Text_object/text3.md)

[text.border](./Text_object/text4.md)

[text.description](./Text_object/text5.md)

[text.embeddedCharacters](./Text_object/text6.md)

[text.embedRanges](./Text_object/text7.md)

[text.embedVariantGlyphs](./Text_object/text8.md)

[text.filters](./Text_object/text9.md)

[text.fontRenderingMode](./Text_object/text10.md)

[text.getTextAttr()](./Text_object/text11.md)

[text.getTextString()](./Text_object/text12.md)

[text.length](./Text_object/text13.md)

[text.lineType](./Text_object/text14.md)

[text.maxCharacters](./Text_object/text15.md)

[text.orientation](./Text_object/text16.md)

[text.renderAsHTML](./Text_object/text17.md)

[text.scrollable](./Text_object/text18.md)

[text.selectable](./Text_object/text19.md)

[text.selectionEnd](./Text_object/text20.md)

[text.selectionStart](./Text_object/text21.md)

[text.setTextAttr()](./Text_object/text22.md)

[text.setTextString()](./Text_object/text23.md)

[text.shortcut](./Text_object/text24.md)

[text.silent](./Text_object/text25.md)

[text.tabIndex](./Text_object/text26.md)

[text.textRuns](./Text_object/text27.md)

[text.textType](./Text_object/text28.md)

[text.useDeviceFonts](./Text_object/text29.md)

[text.variableName](./Text_object/text30.md)


## TextAttrsObject

[textAttrssummary](./TextAttrs_object/textAttrs_summary.md)

[textAttrs.aliasText](./TextAttrs_object/textAttrs.md)

[textAttrs.alignment](./TextAttrs_object/textAttr1.md)

[textAttrs.autoKern](./TextAttrs_object/textAttr2.md)

[textAttrs.bold](./TextAttrs_object/textAttr3.md)

[textAttrs.characterPosition](./TextAttrs_object/textAttr4.md)

[textAttrs.characterSpacing](./TextAttrs_object/textAttr5.md)

[textAttrs.face](./TextAttrs_object/textAttr6.md)

[textAttrs.fillColor](./TextAttrs_object/textAttr7.md)

[textAttrs.indent](./TextAttrs_object/textAttr8.md)

[textAttrs.italic](./TextAttrs_object/textAttr9.md)

[textAttrs.leftMargin](./TextAttrs_object/textAtt10.md)

[textAttrs.letterSpacing](./TextAttrs_object/textAtt11.md)

[textAttrs.lineSpacing](./TextAttrs_object/textAtt12.md)

[textAttrs.rightMargin](./TextAttrs_object/textAtt13.md)

[textAttrs.rotation](./TextAttrs_object/textAtt14.md)

[textAttrs.size](./TextAttrs_object/textAtt15.md)

[textAttrs.target](./TextAttrs_object/textAtt16.md)

[textAttrs.url](./TextAttrs_object/textAtt17.md)


## TextRunObject

[textRunsummary](./TextRun_object/textRun_summary.md)

[textRun.textAttrs](./TextRun_object/textRun.md)

[textRun.characters](./TextRun_object/textRun1.md)


## TextureAtlasExporterobject

[TextureAtlasExporterobjectsummary](./TextureAtlasExporter_object/TextureAtlasExporter_summary.md)

[TextureAtlasExporter.algorithm](./TextureAtlasExporter_object/TextureAtlasExporter.md)

[TextureAtlasExporter.allowRotate](./TextureAtlasExporter_object/TextureAtlasExporter1.md)

[TextureAtlasExporter.app](./TextureAtlasExporter_object/TextureAtlasExporter2.md)

[TextureAtlasExporter.autoSize](./TextureAtlasExporter_object/TextureAtlasExporter3.md)

[TextureAtlasExporter.borderPadding](./TextureAtlasExporter_object/TextureAtlasExporter4.md)

[TextureAtlasExporter.canRotate](./TextureAtlasExporter_object/TextureAtlasExporter5.md)

[TextureAtlasExporter.exportTextureAtlas()](./TextureAtlasExporter_object/TextureAtlasExporter6.md)

[TextureAtlasExporter.filePath](./TextureAtlasExporter_object/TextureAtlasExporter7.md)

[TextureAtlasExporter.flattenSkewObject](./TextureAtlasExporter_object/TextureAtlasExporter8.md)

[TextureAtlasExporter.imageFormat](./TextureAtlasExporter_object/TextureAtlasExporter9.md)

[TextureAtlasExporter.optimizeBitmap](./TextureAtlasExporter_object/TextureAtlasExporter10.md)

[TextureAtlasExporter.optimizeJson](./TextureAtlasExporter_object/TextureAtlasExporter11.md)

[TextureAtlasExporter.overflowed](./TextureAtlasExporter_object/TextureAtlasExporter12.md)

[TextureAtlasExporter.resolution](./TextureAtlasExporter_object/TextureAtlasExporter13.md)

[TextureAtlasExporter.shapePadding](./TextureAtlasExporter_object/TextureAtlasExporter14.md)

[TextureAtlasExporter.sheetHeight](./TextureAtlasExporter_object/TextureAtlasExporter15.md)

[TextureAtlasExporter.sheetWidth](./TextureAtlasExporter_object/TextureAtlasExporter16.md)

[TextureAtlasExporter.version](./TextureAtlasExporter_object/TextureAtlasExporter17.md)


## TimelineObject

[timelinesummary](./Timeline_object/timeline_summary.md)

[timeline.addMotionGuide()](./Timeline_object/timeline.md)

[timeline.addNewLayer()](./Timeline_object/timelin1.md)

[timeline.advancedLayersEnabled](./Timeline_object/timeli52.md)

[timeline.clearFrames()](./Timeline_object/timelin2.md)

[timeline.clearKeyframes()](./Timeline_object/timelin3.md)

[timeline.convertToBlankKeyframes()](./Timeline_object/timelin4.md)

[timeline.convertToKeyframes()](./Timeline_object/timelin5.md)

[timeline.copyFrames()](./Timeline_object/timelin6.md)

[timeline.copyLayers()](./Timeline_object/timelin7.md)

[timeline.copyMotion()](./Timeline_object/timelin8.md)

[timeline.copyMotionAsAS3()](./Timeline_object/timelin9.md)

[timeline.createMotionObject()](./Timeline_object/timeli10.md)

[timeline.createMotionTween()](./Timeline_object/timeli11.md)

[timeline.currentFrame](./Timeline_object/timeli12.md)

[timeline.currentLayer](./Timeline_object/timeli13.md)

[timeline.cutFrames()](./Timeline_object/timeli14.md)

[timeline.cutLayers()](./Timeline_object/timeli15.md)

[timeline.deleteLayer()](./Timeline_object/timeli16.md)

[timeline.duplicateLayers()](./Timeline_object/timeli17.md)

[timeline.expandFolder()](./Timeline_object/timeli18.md)

[timeline.findLayerIndex()](./Timeline_object/timeli19.md)

[timeline.frameCount](./Timeline_object/timeli20.md)

[timeline.getBounds()](./Timeline_object/timeli21.md)

[timeline.getFrameProperty()](./Timeline_object/timeli22.md)

[timeline.getGuidelines()](./Timeline_object/timeli23.md)

[timeline.getLayerProperty()](./Timeline_object/timeli24.md)

[timeline.getSelectedFrames()](./Timeline_object/timeli25.md)

[timeline.getSelectedLayers()](./Timeline_object/timeli26.md)

[timeline.insertBlankKeyframe()](./Timeline_object/timeli27.md)

[timeline.insertFrames()](./Timeline_object/timeli28.md)

[timeline.insertKeyframe()](./Timeline_object/timeli29.md)

[timeline.layerCount](./Timeline_object/timeli30.md)

[timeline.layers](./Timeline_object/timeli31.md)

[timeline.libraryItem](./Timeline_object/timeli32.md)

[timeline.mergeLayers()](./Timeline_object/timeli51.md)

[timeline.name](./Timeline_object/timeli33.md)

[timeline.pasteFrames()](./Timeline_object/timeli34.md)

[timeline.pasteLayers()](./Timeline_object/timeli35.md)

[timeline.pasteMotion()](./Timeline_object/timeli36.md)

[timeline.pasteMotionSpecial()](./Timeline_object/timeli37.md)

[timeline.removeFrames()](./Timeline_object/timeli38.md)

[timeline.removeMotionObject()](./Timeline_object/timeli39.md)

[timeline.reorderLayer()](./Timeline_object/timeli40.md)

[timeline.reverseFrames()](./Timeline_object/timeli41.md)

[timeline.selectAllFrames()](./Timeline_object/timeli42.md)

[timeline.setFrameProperty()](./Timeline_object/timeli43.md)

[timeline.setGuidelines()](./Timeline_object/timeli44.md)

[timeline.setLayerProperty()](./Timeline_object/timeli45.md)

[timeline.setSelectedFrames()](./Timeline_object/timeli46.md)

[timeline.setSelectedLayers()](./Timeline_object/timeli47.md)

[timeline.showLayerMasking()](./Timeline_object/timeli48.md)

[timeline.startPlayback()](./Timeline_object/timeli49.md)

[timeline.stopPlayback()](./Timeline_object/timeli50.md)


## ToolObjobject

[toolObjsummary](./ToolObj_object/toolObj_summary.md)

[toolObj.depth](./ToolObj_object/toolObj.md)

[toolObj.enablePIControl()](./ToolObj_object/toolObj1.md)

[toolObj.iconID](./ToolObj_object/toolObj2.md)

[toolObj.position](./ToolObj_object/toolObj3.md)

[toolObj.setIcon()](./ToolObj_object/toolObj4.md)

[toolObj.setMenuString()](./ToolObj_object/toolObj5.md)

[toolObj.setOptionsFile()](./ToolObj_object/toolObj6.md)

[toolObj.setPI()](./ToolObj_object/toolObj7.md)

[toolObj.setToolName()](./ToolObj_object/toolObj8.md)

[toolObj.setToolTip()](./ToolObj_object/toolObj9.md)

[toolObj.showPIControl()](./ToolObj_object/toolOb10.md)

[toolObj.showTransformHandles()](./ToolObj_object/toolOb11.md)


## ToolsObject

[toolssummary](./Tools_object/tools_summary.md)

[tools.activeTool](./Tools_object/tools.md)

[tools.altIsDown](./Tools_object/tools1.md)

[tools.constrainPoint()](./Tools_object/tools2.md)

[tools.ctlIsDown](./Tools_object/tools3.md)

[tools.getKeyDown()](./Tools_object/tools4.md)

[tools.mouseIsDown](./Tools_object/tools5.md)

[tools.penDownLoc](./Tools_object/tools6.md)

[tools.penLoc](./Tools_object/tools7.md)

[tools.setCursor()](./Tools_object/tools8.md)

[tools.shiftIsDown](./Tools_object/tools9.md)

[tools.snapPoint()](./Tools_object/tools10.md)

[tools.toolObjs](./Tools_object/tools11.md)


## TweenObject

[TweenobjectSummary](./Tween_Object/Tween_object_Summary.md)

[Tween.getColorTransform(()](./Tween_Object/Tween.md)

[Tween.getFilters(()](./Tween_Object/Tween1.md)

[Tween.getGeometricTransform()](./Tween_Object/Tween2.md)

[Tween.getShape(()](./Tween_Object/Tween3.md)

[Tween.duration](./Tween_Object/Tween4.md)

[Tween.startFrame](./Tween_Object/Tween5.md)

[Tween.tweenType](./Tween_Object/Tween6.md)


## Vertexobject

[vertexsummary](./Vertex_object/vertex_summary.md)

[vertex.getHalfEdge()](./Vertex_object/vertex.md)

[vertex.setLocation()](./Vertex_object/vertex1.md)

[vertex.x](./Vertex_object/vertex2.md)

[vertex.y](./Vertex_object/vertex3.md)


## VideoItemObject

[videoItemsummary](./VideoItem_object/videoItem_summary.md)

[videoItem.exportToFLV()](./VideoItem_object/videoItem.md)

[videoItem.fileLastModifiedDate](./VideoItem_object/videoIte1.md)

[videoItem.lastModifiedDate](./VideoItem_object/videoIte2.md)

[videoItem.sourceFileExists](./VideoItem_object/videoIte3.md)

[videoItem.sourceFileIsCurrent](./VideoItem_object/videoIte4.md)

[videoItem.sourceFilePath](./VideoItem_object/videoIte5.md)

[videoItem.videoType](./VideoItem_object/videoIte6.md)


## XMLUIObject

[xmluisummary](./XMLUI_object/xmlui_summary.md)

[xmlui.accept()](./XMLUI_object/xmlui.md)

[xmlui.cancel()](./XMLUI_object/xmlui1.md)

[xmlui.get()](./XMLUI_object/xmlui2.md)

[xmlui.getControlItemElement()](./XMLUI_object/xmlui3.md)

[xmlui.getEnabled()](./XMLUI_object/xmlui4.md)

[xmlui.getVisible()](./XMLUI_object/xmlui5.md)

[xmlui.set()](./XMLUI_object/xmlui6.md)

[xmlui.setControlItemElement()](./XMLUI_object/xmlui7.md)

[xmlui.setControlItemElements()](./XMLUI_object/xmlui8.md)

[xmlui.setEnabled()](./XMLUI_object/xmlui9.md)

[xmlui.setVisible()](./XMLUI_object/xmlui10.md)


## C-LevelExtensibility

[Aboutextensibility](./C-Level_Extensibility/About_extensibility.md)

[IntegratingCfunctions](./C-Level_Extensibility/Integrating_C_functions.md)

[Datatypes](./C-Level_Extensibility/Data_types.md)

[TheC-levelAPI](./C-Level_Extensibility/The_C.md)
