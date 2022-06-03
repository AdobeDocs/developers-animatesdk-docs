---
title: Animate JSAPI Documentation
description: This is the home page of Animate APIs

---

# Animate JSAPI Documentation

## Table of Contents

 - [Introduction](#introduction)
  	* [Working with the JavaScript API](#working-with-the-javascript-api)
  	* [Creating JSFL files](#creating-jsfl-files)
  	* [Saving JSFL files](#saving-jsfl-files)
  	* [Running scripts](#running-scripts)
  	* [What’s new in the JavaScript API](#whats-new-in-the-javascript-api)
  	* [JavaScript API objects](#javascript-api-objects)
  	* [Specifying the target of an action](#specifying-the-target-of-an-action)
  	* [Summary of the DOM structure](#summary-of-the-dom-structure)
  	* [Sample implementations](#sample-implementations)
 - [Top-Level Functions and Methods](#top-level-functions-and-methods-1)
 - [actionsPanel Object](#actionspanel-object)
 - [bitmapInstance Object](#bitmapinstance-object)
 - [bitmapItem Object](#bitmapitem-object)
 - [camera Object](#camera-object)
 - [compiledClipInstance Object](#compiledclipinstance-object)
 - [compilerErrors Object](#compilererrors-object)
 - [componentInstance Object](#componentinstance-object)
 - [componentsPanel Object](#componentspanel-object)
 - [contour Object](#contour-object)
 - [document Object](#document-object)
 - [drawingLayer](#drawinglayer)
 - [edge Object](#edge-object)
 - [element Object](#element-object)
 - [fill Object](#fill-object)
 - [filter Object](#filter-object)
 - [flash(fl.()) Object](#flashfl-object)
 - [FLfile Object](#flfile-object)
 - [folderItem Object](#folderitem-object)
 - [fontItem Object](#fontitem-object)
 - [frame Object](#frame-object)
 - [HalfEdge Object](#halfedge-object)
 - [Instance Object](#instance-object)
 - [Item Object](#item-object)
 - [Layer Object](#layer-object)
 - [LayerParenting Object](#layerparenting-object)
 - [library Object](#library-object)
 - [Math Object](#math-object)
 - [Matrix Object](#matrix-object)
 - [outputPanel Object](#outputpanel-object)
 - [Oval Object](#oval-object)
 - [Parameter object](#parameter-object)
 - [Path object](#path-object)
 - [presetItem object](#presetitem-object)
 - [presetPanel object](#presetpanel-object)
 - [Rectangle object](#rectangle-object)
 - [Shape object](#shape-object)
 - [SoundItem object](#sounditem-object)
 - [SpriteSheetExporter object](#spritesheetexporter-object)
 - [Stroke object](#stroke-object)
 - [swfPanel object](#swfpanel-object)
 - [SymbolInstance object](#symbolinstance-object)
 - [SymbolItem object](#symbolitem-object)
 - [Text Object](#text-object)
 - [TextAttrs Object](#textattrs-object)
 - [TextRun Object](#textrun-object)
 - [TextureAtlasExporter object](#textureatlasexporter-object)
 - [Timeline Object](#timeline-object)
 - [ToolObj object](#toolobj-object)
 - [Tools Object](#tools-object)
 - [Tween Object](#tween-object)
 - [Vertex object](#vertex-object)  
 - [VideoItem Object](#videoitem-object)
 - [XMLUI Object](#xmlui-object)
 - [C-LevelExtensibility](#c-levelextensibility)
        

## Introduction

### Working with the JavaScript API

As a user of Adobe® Animate®, you may be familiar with Adobe® ActionScript®, which lets you create scripts that execute at run time in Adobe® Flash® Player. The Animate JavaScript application programming interface (JavaScript API or JSAPI) described in this document is a complementary programming tool that lets you create scripts that run in the Animate authoring environment.

This document describes the objects, methods, and properties available in the JavaScript API. It assumes that you know how to use the documented commands when working in the authoring environment. If you have a question about what a particular command does, use other documents in Animate Help, such as *Using Animate*, to find that information.

This document also assumes that you are familiar with JavaScript or ActionScript syntax and with basic programming concepts such as functions, parameters, and data types.

The Animate JavaScript API lets you write scripts to perform several actions in the Animate authoring environment (that is, while a user has the Animate program open). This functionality is different from the ActionScript language, which lets you write scripts to perform actions in the Flash Player environment (that is, while a SWF file is playing). This functionality is also different from JavaScript commands that you might use in pages displayed in a web browser.

Using the JavaScript API, you can write Animate application scripts to help streamline the authoring process. For example, you can write scripts to automate repetitive tasks or add custom tools to the Tools panel.

The Animate JavaScript API is designed to resemble the Adobe® Dreamweaver® and Adobe® Fireworks® JavaScript API (which were designed based on the Netscape JavaScript API). The Animate JavaScript API is based on a Document Object Model (DOM), which allows Animate documents to be accessed using JavaScript objects. The Animate JavaScript API includes all elements of the Netscape JavaScript API, plus the Animate DOM. These added objects and their methods and properties are described in this document. You can use any of the elements of the native JavaScript language in an Animate script, but only elements that make sense in the context of an Animate document have an effect.

The JavaScript API also contains methods that let you implement extensibility using a combination of JavaScript and custom C code. For more information, see [C-Level Extensibility](/C-Level_Extensibility/About_extensibility.md).

The JavaScript interpreter in Animate is the Mozilla SpiderMonkey engine, version 1.8. SpiderMonkey is one of the two reference implementations of the JavaScript language developed by Mozilla.org. It is the same engine that is embedded in the Mozilla browser.

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



### What’s new in the JavaScript API

The following section lists new objects, methods, and properties in Animate. It also lists changes in Flash CC, CS6, CS5.5, and CS5.
If you have not used the JavaScript API before, you might want to skip this section and go directly to [JavaScript API objects](/Introduction/JavaScript_API_objects.md).

#### New methods and properties in Animate 2020
The following methods and properties for existing objects are new in Animate 2020:

-   [Document object](/Document_object/document_summary.md)

    -   [document.getTaggedSwatches()](/Document_object/docu6064.md)

    -   [document.getTaggedSwatchByName()](/Document_object/docu6062.md)

    -   [document.getTaggedSwatchAtIndex()](/Document_object/docu6061.md)

    -   [document.setTaggedSwatchByName()](/Document_object/docu6068.md)

    -   [document.setTaggedSwatchAtIndex()](/Document_object/docu6067.md)

    -   [document.addTaggedSwatch()](/Document_object/docu6058.md)

    -   [document.addTaggedSwatchWithColor()](/Document_object/docu6059.md)

    -  [document.deleteTaggedSwatchByName()](/Document_object/docu6066.md)

    -   [document.deleteTaggedSwatchAtIndex()](/Document_object/docu6065.md)

    -   [document.getTaggedSwatchesPaletteList()](/Document_object/docu6063.md)

    -   [document.getIndexForTaggedSwatchesPalette()](/Document_object/docu6060.md)

    -   [document.convertToDoc()](/Document_object/docu6069.md)

    -   [document.exportCanvasPublishTemplate()](/Document_object/docu6070.md)

    -   [document.importCanvasPublishTemplate()](/Document_object/docu6071.md)

    -  [document.exportMedia()](/Document_object/docu6072.md)

    -   [document.exportSVG()](/Document_object/docu6074.md)

-   [Layer object](/Layer_object/layer_summary.md)

    -   [layer.getZDepthAtFrame()](/Layer_object/layer11.md)

    -   [layer.setZDepthAtFrame()](/Layer_object/layer12.md)

    -   [layer.getRigParentAtFrame()](/Layer_Parenting_Object/layerParenting1.md)

    -   [layer.setRigParentAtFrame()](/Layer_Parenting_Object/layerParenting2.md)

    -   [layer.getRigMatrixAtFrame()](/Layer_Parenting_Object/layerParenting3.md)

    -   [layer.getFiltersAtFrame()](/Layer_object/layer15.md)

    -   [layer. setFiltersAtFrame()](/Layer_object/layer18.md)

    -   [layer.getColorTransformAtFrame()](/Layer_object/layer14.md)

    -   [layer.setColorTransformAtFrame()](/Layer_object/layer17.md)

    -   [layer.getBlendModeAtFrame()](/Layer_object/layer13.md)

    -   [layer.setBlendModeAtFrame()](/Layer_object/layer16.md)

-   [Timeline object](/Timeline_object/timeline_summary.md)

    -   [timeline.advancedLayersEnabled](/Timeline_object/timeli52.md)

    -   [timeline.mergeLayers()](/Timeline_object/timeli51.md)

-   [flash object (fl)](/flash_object_(fl)/fl_summary.md)

    -   [fl.addToolInToolbar()](/flash_object_(fl)/fl82.md)


#### New objects in Animate 2020
The following object is new in Flash CS6:

-   [TextureAtlasExporter object](/TextureAtlasExporter_object/TextureAtlasExporter_summary.md)

-   [Camera object](/Camera_object/Camera_Summary.md)

#### New methods and properties in Flash CC

The following methods and properties for existing objects are new in Flash Profesional CC:

-   [Tween Object](/Tween_Object/Tween_object_Summary.md)

    -   Tween.getColorTransform( )

    -   Tween.getFilters( )

    -   Tween.getGeometricTransform()

    -   Tween.getShape( )

    -   Tween.duration

    -   Tween.startFrame

    -   Tween.tweenType

-   [CompiledClipInstance object](/CompiledClipInstance_object/compiledClipInstance_summary.md)

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

-   [Document object](/Document_object/document_summary.md)

    -   Document.convertSelectionToBitmap()

    -   Document.distributeToKeyframes()

    -   Document.exportVideo()

    -   Document.getPublishDocumentData()

    -   Document.getTelemetryForSwf()

    -   Document.importFile() showDialog and showImporterUI properties

    -   Document.setPublishDocumenData()

-   [Element object](/Element_object/element_summary.md)

    -   Element.getPublishPersistentData()

    -   Element.setPublishPersistentData()

-   [flash object (fl)](/flash_object_(fl)/fl_summary.md)

    -   Flash.addEventListener()prePublish, postPublish, selectionChanged, and dpiChanged events

    -   fl.getThemeColor()

    -   fl.getThemeColorParameters()

    -   fl.getThemeFontInfo()

    -   fl.setPrefBoolean()

    -   fl.toggleBreakPoint()

    -   fl.xmlPanel()

    -   fl.xmlPanelFromString()

-   [Frame object](/Frame_object/frame_summary.md)

    -   Frame.convertToFrameByFrameAnimation()

    -   Frame.getSoundEnvelope()

    -   Frame.getSoundEnvelopeLimits()

    -   Frame.setSoundEnvelope()

    -   Frame.setSoundEnvelopeLimits()

    -   Frame.isEmpty()

-   [Item object](/Item_object/item_summary.md)

    -   item.getPublishData()

    -   item.setPublishData()

-   [library object](/library_object/library_summary.md)

    -   library.unusedItems

-   [swfPanel object](/swfPanel_object/swfPanel_summary.md)

    -   swfPanel.dpiScaleFactorX

    -   swfPanel.dpiScaleFactorY

    -   swfPanel.reload()

-   [SymbolInstance object](/SymbolInstance_object/symbolInstance_summary.md)

    -   SymbolInstance.brightness

    -   SymbolInstance.tintColor

    -   SymbolInstance.tintPercent

-   [Timeline object](/Timeline_object/timeline_summary.md)

    -   getBounds()

#### Dropped methods and properties in Flash CC

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

#### New objects in Flash CS6

The following object is new in Flash CS6:

-   [SpriteSheetExporter object](/SpriteSheetExporter_object/SpriteSheetExporter_summary.md)

#### New methods and properties in Flash CS6

The following methods and properties for existing objects are new in Flash Pro CS6:

-   [BitmapItem object](/BitmapItem_object/bitmapItem_summary.md)

    -   bitmapItem.exportToFile()quality parameter

    -   bitmapItem.hasValidAlphaLayer

    -   bitmapItem.lastModifiedDate

-   [Document object](/Document_object/document_summary.md)

    -   document.exportInstanceToLibrary()

    -   document.exportInstanceToPNGSequence()

    -   document.getSWFPathFromProfile()

    -   document.saveAsCopy()

    -   document.swfJPEGQuality

-   [flash object (fl)](/flash_object_(fl)/fl_summary.md)

    -   fl.spriteSheetExporter

-   [Layer object](/Layer_object/layer_summary.md)

    -   layer.animationType

-   [Math object](/Math_object/Math_summary.md)

    -   Math.transformPoint()

-   [Shape object](/Shape_object/shape_summary.md)

    -   shape.isFloating

-   [SoundItem object](/SoundItem_object/soundItem_summary.md)

    -   soundItem.lastModifiedDate

-   [SymbolInstance object](/SymbolInstance_object/symbolInstance_summary.md)

    -   symbolInstance.is3D

-   [SymbolItem object](/SymbolItem_object/symbolItem_summary.md)

    -   symbolItem.exportToLibrary()

    -   symbolItem.exportToPNGSequence()

    -   symbolItem.lastModifiedDate

-   [Text object](/Text_object/text_summary.md)

    -   text.filters

-   [VideoItem object](/VideoItem_object/videoItem_summary.md)

    -   videoItem.lastModifiedDate

#### New methods and properties in Flash CS5 and CS5.5

The following methods and properties for existing objects are new in Flash Pro CS5:

-   [Document object](/Document_object/document_summary.md)

    -   document.debugMovie()

    -   document.loadCuepointXML()

-   [flash object (fl)](/flash_object_(fl)/fl_summary.md)

    -   fl.languageCode

    -   fl.toggleBreakpoint

-   [Frame object](/Frame_object/frame_summary.md)

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

-   [Timeline object](/Timeline_object/timeline_summary.md)

    -   timeline.createMotionObject()

    -   timeline.libraryItem

    -   timeline.removeMotionObject()

    -   timeline.startPlayback

    -   timeline.stopPlayback

The following methods and properties for existing objects are new in Flash Pro CS5.5:

-   [SymbolInstance object](/SymbolInstance_object/symbolInstance_summary.md)

    -   symbolInstance.bitmapRenderMode

    -   symbolInstance.backgroundColor

    -   symbolInstance.usesBackgroundColor

    -   symbolInstance.visible

-   [Timeline object](/Timeline_object/timeline_summary.md)

    -   timeline.copyLayers()

    -   timeline.cutLayers()

    -   timeline.duplicateLayers()

    -   timeline.pasteLayers()

-   [flash object (fl)](/flash_object_(fl)/fl_summary.md)

    -   fl.getSwfPanel()

    -   fl.installedPlayers()

    -   fl.publishCacheEnabled

    -   fl.publishCacheDiskSizeMax

    -   fl.publishCacheMemorySizeMax

    -   fl.publishCacheMemoryEntrySizeLimit

    -   fl.clearPublishCache()

-   [swfPanel object](/swfPanel_object/swfPanel_summary.md)

    -   swfPanel.setFocus()

#### Other changes in Flash CS5 and CS5.5

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





### JavaScript API objects

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

#### The Animate Document Object Model

The Animate Document Object Model (DOM) for the Animate JavaScript API consists of a set of top-level functions (see ["Top-Level Functions and Methods"](/Top-Level_Functions_and_Methods/Top.md)) and two top-level objects—the FLfile object and the flash object (an or fl). Each object is guaranteed to be available to a script because it always exists when the Animate authoring environment is open. For more information, see [FLfile object](/FLfile_object/FLfile_summary.md) and [flash object (fl)](/flash_object_(fl)/fl_summary.md).
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

#### The Document object

An important property of the top-level flash object is the [fl.documents](/flash_object_(fl)/fl20.md) property. This property contains an array of Document objects, each of which represents one of the FLA files currently open in the authoring environment. The properties of each Document object represent most of the elements that a FLA file can contain. Therefore, a large portion of the DOM is composed of child objects and properties of the Document object. For more information, see [Document object](/Document_object/document_summary.md).

To refer to the first open document, for example, use the statement ```flash.documents[0]``` or ```fl.documents[0]```. The first document is the first Animate document that was opened during the current session in the authoring environment. When the first opened document is closed, the indexes of the other open documents are decremented.

To find a particular document’s index, use ```flash.findDocumentIndex(nameOfDocument)``` or ```fl.findDocumentIndex(nameOfDocument)```. See [fl.findDocumentIndex()](/flash_object_(fl)/fl26.md).

To access the document that is currently focused, use the statement ```flash.getDocumentDOM()``` or ```fl.getDocumentDOM()```. See [fl.getDocumentDOM()](/flash_object_(fl)/fl31.md). The latter is the syntax used in most of the examples in this document.

To find a particular document in the fl.documents array, iterate through the array and test each document for its
```document.name``` property. See [fl.documents](/flash_object_(fl)/fl20.md) and [document.name](/Document_object/docum170.md).

All the objects in the DOM that aren’t listed in the previous table (see ["The Animate Document Object Model"](#the-animate-document-object-model)) are accessed from the Document object. For example, to access the library of a document, you use the ```document.library``` property, which retrieves a library object:

```fl.getDocumentDOM().library```

To access the array of items in the library, you use the ```library.items``` property; each element in the array is an Item object:

```fl.getDocumentDOM().library.items```

To access a particular item in the library, you specify a member of the library.items array:

```fl.getDocumentDOM().library.items[0]```

In other words, the library object is a child of the Document object, and the Item object is a child of the library object. For more information, see [document.library](/Document_object/docume98.md), [library object](/library_object/library_summary.md), [library.items](/library_object/librar10.md) and [Item object](/Item_object/item_summary.md).

### Specifying the target of an action

Unless otherwise specified, methods affect the current focus or selection. For example, the following script doubles the size of the current selection because no particular object is specified:

```fl.getDocumentDOM().scaleSelection(2, 2);```

In some cases, you might want an action to specifically target the currently selected item in the Animate document. To do this, use the array that the ```document.selection``` property contains (see [document.selection](/Document_object/docum430.md)). The first element in the array represents the currently selected item, as shown in the following example:

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


#### Top-Level Functions and Methods 
01 [FLfile object](#flfile-object)

01 [flash object (fl)](#flashfl-object)

   02 [compilerErrors object](#compilererrors-object)

   02 [componentsPanel object](#componentspanel-object)

   02 [Document object (fl.documents array)](#document-object)

   02 [Filter object](#filter-object)
   -  [Matrix object](#matrix-object)
   - [Fill object](#fill-object)
   - [Stroke object](#stroke-object)

   - [library object](#library-object)

        * [Item object (library.items array)](#item-object)

        * [BitmapItem object(subclass of Item object) ](#bitmapitem-object)

        * [folderItem object (subclass of Item object) ](#folderitem-object)

        * [fontItem object (subclass of Item object) ](#fontitem-object)

        * [SoundItem object (subclass of Item object) ](#sounditem-object)

        * [SymbolItem object (subclass of Item object) ](#symbolitem-object)

        * [VideoItem object (subclass of Item object)](#videoitem-object)

   - [Timeline object (document.timelines array) ](#timeline-object)

   - [Layer object (timeline.layers array)](#layer-object)

        - [Frame object (layer.frames array)](#frame-object)

        - [Element object (frame.elements array) ](#element-object)

   - [Matrix object (element.matrix)](#matrix-object)

   - [Instance object (abstract class, subclass of Element object) ](#instance-object)

   - [BitmapInstance object (subclass of Instance object)](#bitmapinstance-object)

   - [CompiledClipInstance object (subclass of Instance object)](#compiledclipinstance-object)

   - [ComponentInstance object (subclass of SymbolInstance object) ](#componentinstance-object)

   - [Parameter object (componentInstance.parameters array)](#parameter-object)

   - [SymbolInstance object (subclass of Instance object) ](#symbolinstance-object)

   - [Text object (subclass of Element object)](#text-object)

   - [TextRun object (text.textRuns array)](#textrun-object)

   - [TextAttrs object (textRun.textAttrs array) ](#textattrs-object)

   - [Shape object (subclass of Element object)](#shape-object)

   - [Oval object](#oval-object)

   - [Rectangle object](#rectangle-object)

   - [Contour object (shape.contours array) ](#contour-object)

   - [HalfEdge object](#halfedge-object)

   - [Vertex object](#vertex-object)

   - [Edge object](#edge-object)

   - [Edge object (shape.edges array) ](#edge-object)

   - [HalfEdge object](#halfedge-object)

   - [Parameter object (screen.parameters array) ](#parameter-object)

 02 [drawingLayer object](#drawinglayer)

   * [Path object](#path-object)

        - [Contour object](#contour-object)

 02 [Math object](#math-object)

 02 [outputPanel object](#outputpanel-object)

 02 [presetPanel object](#presetpanel-object)

- [presetItem object ](#presetitem-object)

 02 [swfPanel object](#swfpanel-object)

 02 [Tools object (fl.tools array)](#tools-object)

   * [ToolObj object (tools.toolObjs array) ](#toolobj-object)

 02 [XMLUI object](#xmlui-object)
    


### Sample implementations

Several sample JSFL implementations are available for Adobe Animate. You can review and install these files to familiarize yourself with the JavaScript API. The samples are in a folder named Samples within the [Samples.zip](https://github.com/AdobeDocs/developers-animatesdk-docs/raw/master/downloads/Samples.zip).

#### Sample Shape command

A sample JavaScript API script named Shape.jsfl is located in the Shape folder (see "Sample implementations" above). This script displays information about the contours of the shape in the Output panel.

#### To install and run the Shape script:

1.  Copy the Shape.jsfl file to the Configuration > Commands folder (see ["Saving JSFL files"](/Introduction/Working_with_the_JavaScript_API.md#saving-jsfl-files)).

2.  In a Animate document (FLA file), select a shape object.

3.  Select Commands > Shape to run the script.

#### Sample get and set filters command

A sample JavaScript API script named filtersGetSet.jsfl is located in the filtersGetSet folder (see "Sample implementations" above). This script adds filters to a selected object and displays information about the filters being added in the Output panel.

#### To install and run the filtersGetSet script:

1.  Copy the filtersGetSet.jsfl file to the Configuration/Commands folder (see ["Saving JSFL files"](/Introduction/Working_with_the_JavaScript_API.md#saving-jsfl-files)).

2.  In a Animate document (FLA file), select a text, movie clip, or button object.

3.  Select Commands > filtersGetSet to run the script.

#### Sample PolyStar tool

A sample JavaScript API script named PolyStar.jsfl is located in the PolyStar folder (see "Sample implementations" above).
The PolyStar.jsfl replicates the PolyStar tool that can be found in the Animate Tools panel. The script demonstrates how to build the PolyStar tool using the JavaScript API and includes detailed comments describing what the code is doing. Read this file to gain a better understanding of how the JavaScript API can be used. You should also read the PolyStar.xml file in the Tools directory to learn more about how to build your own tool.

#### Sample Trace Bitmap panel

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

#### Sample DLL

A sample DLL implementation is located in the dllSampleComputeSum folder (see "Sample implementations" above). For more information about building DLLs, see[ "C-Level Extensibility"](/C-Level_Extensibility/About_extensibility.md).




## Top-Level Functions and Methods

#### About this section


This section describes the top-level functions and methods that are available when you use the Adobe Flash JavaScript application programming interface (JavaScript API). For information about where to store JavaScript API files, see ["Saving JSFL files"](/Introduction/Working_with_the_JavaScript_API.md#saving-jsfl-files).


#### Global methods

The following methods can be called from any JavaScript API script:
alert()
confirm()
prompt()

#### Extensible tools

The following functions are available in scripts that create extensible tools:
activate()
configureTool()
deactivate()
keyDown()
keyUp()
mouseDoubleClick()
mouseDown()
mouseMove()
mouseUp()
notifySettingsChanged()
setCursor()



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


## actionsPanel Object

#### Availability

Flash CS3 Professional.

#### Description

The actionsPanel object, which represents the currently displayed Actions panel, is a property of the Animate object (see [fl.actionsPanel](/flash_object_(fl)/fl.md)).

#### Method summary

The following methods can be used with the actionsPanel object:

| **Method**                                                                                                                           | **Description**                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [actionsPanel.getClassForObject() -dropped](/actionsPanel_object/actionsPanel.md) | Dropped in Adobe Animate.                                              |
| [actionsPanel.getScriptAssistMode() -dropped](/actionsPanel_object/actionsPane1.md)                                                         | Dropped in Adobe Animate.                                              |
| [actionsPanel.getSelectedText()](/actionsPanel_object/actionsPane2.md)                                                                                       | Returns the text that is currently selected in the Actions panel.      |
| [actionsPanel.getText()](/actionsPanel_object/actionsPane3.md)                                                                                               | Returns the text in the Actions panel.                                 |
| [actionsPanel.hasSelection()](/actionsPanel_object/actionsPane4.md)                                                                                          | Specifies whether any text is currently selected in the Actions panel. |
| [actionsPanel.replaceSelectedText()](/actionsPanel_object/actionsPane5.md)                                                                                   | Replaces the currently selected text with specified text.              |
| [actionsPanel.setScriptAssistMode() -dropped](/actionsPanel_object/actionsPane6.md)                                                         | Dropped in Adobe Animate.                                              |
| [actionsPanel.setSelection()](/actionsPanel_object/actionsPane7.md)                                                                                          | Selects a specified set of characters in the Actions panel.            |
| [actionsPanel.setText()](/actionsPanel_object/actionsPane8.md)                                                                                               | Clears any text in the Actions panel and then adds specified text.     |

<span id="actionsPanel.getClassForObject()_-_dropp" class="anchor"></span>




## bitmapInstance Object


**Inheritance** [Element object](/Element_object/element_summary.md) > [Instance object](/Instance_object/instance_summary.md) > BitmapInstance object

#### Availability

Flash MX 2004.

#### Description

The BitmapInstance object is a subclass of the Instance object and represents a bitmap in a frame (see [Instance object](/Instance_object/instance_summary.md)).

#### Method summary

In addition to the [Instance object](/Instance_object/instance_summary.md) methods, you can use the following methods with the BitmapInstance object:

| **Method**                                            | **Description**                                                                                                            |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [bitmapInstance.getBits()](/BitmapInstance_object/bitmapInstance.md) | Lets you create bitmap effects by getting the bits out of the bitmap, manipulating them, and then returning them to Animate. |
| [bitmapInstance.setBits()](/BitmapInstance_object/bitmapInstanc2.md)              | Sets the bits of an existing bitmap element.                                                                               |

#### Property summary

In addition to the [Instance object](/Instance_object/instance_summary.md) properties, you can use the following properties with the BitmapInstance object:

| **Property**                           | **Description**                                                            |
|----------------------------------------|----------------------------------------------------------------------------|
| [bitmapInstance.hPixels](/BitmapInstance_object/bitmapInstanc1.md) | Read-only; an integer that represents the width of the bitmap, in pixels.  |
| [bitmapInstance.vPixels](/BitmapInstance_object/bitmapInstanc3.md) | Read-only; an integer that represents the height of the bitmap, in pixels. |

<span id="bitmapInstance.getBits()" class="anchor"></span>





## bitmapItem Object


**Inheritance** [Item object](/Item_object/item_summary.md) > BitmapItem object

#### Availability

Flash MX 2004.

#### Description

A BitmapItem object refers to a bitmap in the library of a document. The BitmapItem object is a subclass of the Item object (see [Item object](/Item_object/item_summary.md)).

#### Property summary

In addition to the [Item object](/Item_object/item_summary.md) properties, the BitmapItem object has following properties:

<table><thead><tr class="header"><th><strong>Property</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/BitmapItem_object/bitmapItem.md">bitmapItem.allowSmoothing</a></td><td>A Boolean value that specifies whether to allow smoothing of a bitmap.</td></tr><tr class="even"><td><a href="/BitmapItem_object/bitmapIte1.md">bitmapItem.compressionType</a></td><td>A string that determines the type of image compression applied to the bitmap.</td></tr><tr class="odd"><td><a href="/BitmapItem_object/bitmapIte3.md">bitmapItem.fileLastModifiedDate</a></td><td>The number of seconds that have elapsed between January 1, 1970 and the modification date of the original file.</td></tr><tr class="even"><td><a href="/BitmapItem_object/bitmapIte4.md">bitmapItem.hasValidAlphaLayer</a></td><td>A Boolean value indicating whether the bitmap has an alpha channel.</td></tr><tr class="odd"><td><a href="/BitmapItem_object/bitmapIte5.md">bitmapItem.hPixels</a></td><td>Specifies the width of the bitmap, in pixels.</td></tr><tr class="even"><td><a href="/BitmapItem_object/bitmapIte6.md">bitmapItem.lastModifiedDate</a></td><td>The modification date of the bitmap item in the Library.</td></tr><tr class="odd"><td><a href="/BitmapItem_object/bitmapIte7.md">bitmapItem.originalCompressionType</a></td><td>Specifies whether the item was imported as an jpeg file.</td></tr><tr class="even"><td><a href="/BitmapItem_object/bitmapIte9.md">bitmapItem.sourceFileExists</a></td><td>Specifies whether the file that was imported to the Library still exists in the location from where it was imported.</td></tr><tr class="odd"><td><a href="/BitmapItem_object/bitmapIt10.md">bitmapItem.sourceFileIsCurrent</a></td><td>Specifies whether the file modification date of the Library item is the same as the modification date on disk of the file that was imported.</td></tr><tr class="even"><td><a href="/BitmapItem_object/bitmapIte11.md">bitmapItem.sourceFilePath</a></td><td>The path and name of the file that was imported into the Library.</td></tr><tr class="odd"><td><a href="/BitmapItem_object/bitmapIte12.md">bitmapItem.useDeblocking</a></td><td><p>Specifies whether deblocking is enabled.</p></td></tr><tr class="even"><td><a href="/BitmapItem_object/bitmapIte13.md">bitmapItem.useImportedJPEGQuality</a></td><td>A Boolean value that specifies whether to use the default imported JPEG quality.</td></tr><tr class="odd"><td><a href="/BitmapItem_object/bitmapIte14.md">bitmapItem.vPixels</a></td><td>Specifies the height of the bitmap, in pixels.</td></tr></tbody></table>

#### Method summary

In addition to the [Item object](/Item_object/item_summary.md) properties, the BitmapItem object has following methods:

| **Method**                                | **Description**                                  |
|-------------------------------------------|--------------------------------------------------|
| [bitmapItem.exportToFile()](/BitmapItem_object/bitmapIte2.md) | Exports the specified item to a PNG or JPG file. |

<span id="bitmapItem.allowSmoothing" class="anchor"></span>




## Camera Object


#### Availability

Adobe Animate 2019

#### Description

This javascript object allows user to access and change properties of camera at any frame in timeline.

Animators can use the following features that are integral to any motion film.

1. Panning with the subject of the frame.

2. Zooming in the object of interest for dramatic effect

3. Zooming out of a frame to remind the viewer of a larger picture

4. Modifying the focal point to shift the attention of the viewer from one subject to another

5. Rotating the camera

6. Using color tint or filters to apply color effects on a scene 

#### Method summary

The following methods can be used with the Camera object:

| **Method**                           | **Description**                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [getZDepth()](/Camera_object/Camera.md)          | Return current Z Depth value of camera.        |
| [getZoom()](/Camera_object/Camera1.md)          | Return the current zoom value of camera. Default is 100%.               |
| [getRotation()](/Camera_object/Camera2.md)          | Return current angle of camera.               |
| [getPosition()](/Camera_object/Camera3.md)     | Return object with x,y, and z properties that specify current location of camera.                                      |
| [getTint()](/Camera_object/Camera4.md)          | Return object with two properties: ‘percent’ & ‘color’.                       |
| [getColorFilter()](/Camera_object/Camera5.md)       | Get camera color filter.                                  |
| [setZDepth()](/Camera_object/Camera6.md)       | Set camera's Z Depth value. |
| [setZoom()](/Camera_object/Camera7.md)        | Zoom camera to absolute value given by input parameter in percentage.                         |
| [setRotation()](/Camera_object/Camera8.md)     | Rotate camera by absolute angle given as input parameters.                              |
| [setTint()](/Camera_object/Camera9.md) | Set camera tint using tint color(RGB) & tint percent (percentage of tint).                    |
| [setColorFilter()](/Camera_object/Camera10.md)            | Set camera color filter using decomposed values of (Brightness,Contrast,saturation,hue).                                             |
| [resetZoom()](/Camera_object/Camera11.md)          | Reset camera zoom to it's default zoom value i.e 100%.                           |
| [resetRotation()](/Camera_object/Camera12.md)       | Reset camera angle to zero.                         |
| [resetPosition()](/Camera_object/Camera13.md)           | Reset camera position to the original position i.e (0,0,0).                                          |
| [resetTint()](/Camera_object/Camera14.md)        | Remove camera tint.                                                       |
| [resetColorFilter()](/Camera_object/Camera15.md)     | Remove color filter.                                |
| [reset()](/Camera_object/Camera16.md)    | Reset all camera properties to default.                       |

#### Property summary

The following properties can be used with the Camera object:

| **Property**                           | **Description**                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [camera.cameraEnabled](/Camera_object/Camera17.md)          |       Enable/Disable camera|
| [camera.colorFilterEnabled](/Camera_object/Camera19.md)          |  Enable/Disable camera's color Filter|   
| [camera.tintEnabled](/Camera_object/Camera18.md)          |     Enable/Disable tint           |            |




<span id="filter.angle" class="anchor"></span>





## compiledClipInstance Object


**Inheritance** [Element object](/Element_object/element_summary.md) > [Instance object](/Instance_object/instance_summary.md) > CompiledClipInstance object

#### Availability

Flash MX 2004.

#### Description

The CompiledClipInstance object is a subclass of the Instance object. It is essentially an instance of a movie clip that has been converted to a compiled clip library item (see [Instance object](/Instance_object/instance_summary.md)).

#### Property summary

In addition to the properties of the [Instance object](/Instance_object/instance_summary.md), the CompiledClipInstance object has the following properties:

| **Property**                                                                | **Description**                                                                           |
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [compiledClipInstance.accName](/CompiledClipInstance_object/compiledClipInstance.md)               | A string that is equivalent to the Name field in the Accessibility panel.                 |
| [compiledClipInstance.actionScript - dropped ](/CompiledClipInstance_object/compiledClipInstanc1.md) | Dropped in Adobe Animate.                                                                 |
| [compiledClipInstance.backgroundColor](/CompiledClipInstance_object/compiledClipInstanc2.md)                        | A string that specifies the matte color when Opaque is selected.                          |
| [compiledClipInstance.description](/CompiledClipInstance_object/compiledClipInstan15.md)                            | A string that is equivalent to the Description field in the Accessibility panel.          |
| [compiledClipInstance.blendMode](/CompiledClipInstance_object/compiledClipInstanc3.md)                              | A string that specifies the blend mode.                                                   |
| [compiledClipInstance.brightness](/CompiledClipInstance_object/compiledClipInstanc4.md)                             | An int that contains the value set in the Color Effect Property Inspector for brightness. |
| [compiledClipInstance.cacheAsBitmap](/CompiledClipInstance_object/compiledClipInstanc5.md)                          | A boolean that indicates whether to cache bitmaps.                                        |
| [compiledClipInstance.colorAlphaAmount](/CompiledClipInstance_object/compiledClipInstanc6.md)      | An int that reduces or increases the tint and alpha values by a constant amount.          |
| [compiledClipInstance.colorAlphaPercent](/CompiledClipInstance_object/compiledClipInstanc7.md)     | An int that reduces the tint and alpha values by a specified percentage.                  |
| [compiledClipInstance.colorBlueAmount](/CompiledClipInstance_object/compiledClipInstanc8.md)                        | An int that reduces or increases the blue tint value by a constant amount.                |
| [compiledClipInstance.colorBluePercent](/CompiledClipInstance_object/compiledClipInstanc9.md)      | An int that reduces the blue tint value by a specified percentage.                        |
| [compiledClipInstance.colorGreenAmount](/lipInstance_object/compiledClipInstan10.md)      | An int that reduces or increases the green tint value by a constant amount.               |
| [compiledClipInstance.colorGreenPercent](/CompiledClipInstance_object/compiledClipInstan11.md)     | An int that reduces the green tint value by a specified percentage.                       |
| [compiledClipInstance.colorMode](/CompiledClipInstance_object/compiledClipInstan12.md)                              | A string that specifies the color mode, as identified in the Symbol Properties dialog.    |
| [compiledClipInstance.colorRedAmount](/CompiledClipInstance_object/compiledClipInstan13.md)                         | An int that reduces or increases the red tint value by a constant amount.                 |
| [compiledClipInstance.colorRedPercent](/CompiledClipInstance_object/compiledClipInstan14.md)                        | An int that reduces the green tint value by a specified percentage.                       |

| **Property**                                                             | **Description**                                                                                                                                                             |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [compiledClipInstance.description](/CompiledClipInstance_object/compiledClipInstan15.md)                         | A string that is equivalent to the Description field in the Accessibility panel.                                                                                            |
| [compiledClipInstance.filters](/CompiledClipInstance_object/compiledClipInstan16.md)                             | An array of Filter objects.                                                                                                                                                 |
| [compiledClipInstance.forceSimple](/CompiledClipInstance_object/compiledClipInstan17.md)                         | A Boolean value that enables and disables the children of the object to be accessible.                                                                                      |
| [compiledClipInstance.shortcut](/CompiledClipInstance_object/compiledClipInstan18.md)                            | A string that is equivalent to the Shortcut field in the Accessibility panel.                                                                                               |
| [compiledClipInstance.silent](/CompiledClipInstance_object/compiledClipInstan19.md)                              | A Boolean value that enables or disables the accessibility of the object; equivalent to the inverse logic of the Make Object Accessible setting in the Accessibility panel. |
| [compiledClipInstance.tabIndex](/CompiledClipInstance_object/compiledClipInstan20.md)                            | An integer that is equivalent to the Tab Index field in the Accessibility panel.                                                                                            |
| [compiledClipInstance.tintColor](/CompiledClipInstance_object/compiledClipInstan21.md)                           | Aa Color object that, when the Color Effect Property Inspector is using style tint, returns the color applied to the tint.                                                  |
| [compiledClipInstance.tintPercent](/CompiledClipInstance_object/compiledClipInstan22.md)                         | A string that, when the Color Effect Property Inspector is using style tint, returns the tint percentage.                                                                   |
| [compiledClipInstance.useBackgroundColor](/CompiledClipInstance_object/compiledClipInstan23.md) | A boolean that sets the background color.                                                                                                                                   |
| [compiledClipInstance.visible](/CompiledClipInstance_object/compiledClipInstan24.md)                             | A boolean that sets visibility.                                                                                                                                             |

<span id="compiledClipInstance.accName" class="anchor"></span>






## compilerErrors Object

#### Availability

Flash CS3 Professional.

#### Description

The compilerErrors object, which represents the Compiler Errors panel, is a property of the flash object (fl) and can be accessed by *fl.compilerErrors* (see [flash object (fl)](/flash_object_(fl)/fl_summary.md
)).

#### Method summary

The following methods can be used with the compilerErrors object:

| **Method**                                        | **Description**                                                       |
|---------------------------------------------------|-----------------------------------------------------------------------|
| [compilerErrors.clear()](/compilerErrors_object/compilerErrors.md) | Clears the contents of the Compiler Errors panel.                     |
| [compilerErrors.save()](/compilerErrors_object/compilerError1.md)             | Saves the contents of the Compiler Errors panel to a local text file. |

<span id="compilerErrors.clear()" class="anchor"></span>




## componentInstance Object


**Inheritance** [Element object](/Element_object/element_summary.md) > [Instance object](/Instance_object/instance_summary.md) > [SymbolInstance object](/SymbolInstance_object/symbolInstance_summary.md) > ComponentInstance object

#### Availability

Flash MX 2004.

#### Description

TheComponentInstance object is a subclass of the SymbolInstance object and represents a component in a frame (see [SymbolInstance object](/SymbolInstance_object/symbolInstance_summary.md)).

#### Property summary

In addition to all the properties of the [SymbolInstance object](/SymbolInstance_object/symbolInstance_summary.md), the ComponentInstance object has the following property:

| **Property**                                                  | **Description**                                                                                               |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [componentInstance.parameters](/ComponentInstance_object/componentInstance.md) | Read-only; an array of ActionScript 2.0 properties that are accessible from the component Property inspector. |

<span id="componentInstance.parameters" class="anchor"></span>




## componentsPanel Object

#### Availability

Flash MX 2004.

#### Description

The componentsPanel object, which represents the Components panel, is a property of the flash object (fl) and can be accessed by *fl.componentsPanel (see [flash object (fl)](/flash_object_(fl)/fl_summary.md))*.

#### Method summary

You can use the following methods with the componentsPanel object:

| **Method**                                                                  | **Description**                                                         |
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [componentsPanel.addItemToDocument()](/componentsPanel_object/componentsPanel.md) | Adds the specified component to the document at the specified position. |
| [componentsPanel.reload()](/componentsPanel_object/componentsPane1.md)                                   | Refreshes the Components panel's list of components.                    |

<span id="componentsPanel.addItemToDocument()" class="anchor"></span>




## contour Object


#### Availability

Flash MX 2004.

#### Description

A Contour object represents a closed path of half edges on the boundary of a shape.

#### Method summary

You can use the following method with the Contour object:

| **Method**                             | **Description**                                                             |
|----------------------------------------|-----------------------------------------------------------------------------|
| [contour.getHalfEdge()](/Contour_object/contour1.md) | Returns a [HalfEdge object](/HalfEdge_object/halfEdge_summary.md) on the contour of the selection. |

#### Property summary

You can use the following properties with the Contour object:

| **Property**                         | **Description**                                                                |
|--------------------------------------|--------------------------------------------------------------------------------|
| [contour.fill](/Contour_object/contour.md)        | A [Fill object](/Fill_object/fill_summary.md).                                                |
| [contour.interior](/Contour_object/contour2.md)    | Read-only; the value is true if the contour encloses an area; false otherwise. |
| [contour.orientation](/Contour_object/contour3.md) | Read-only; an integer indicating the orientation of the contour.               |

<span id="contour.fill" class="anchor"></span>




## document Object


#### Availability

Flash MX 2004.

#### Description

The Document object represents the Stage. That is, only FLA files are considered documents. To return the Document object for the current document, use [fl.getDocumentDOM()](/flash_object_(fl)/fl31.md)

#### Method summary

You can use the following methods with the Document object:

<table><thead><tr class="header"><th><strong>Method</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/Document_object/documen1.md">document.addDataToDocument()</a></td><td>Stores specified data with a document.</td></tr><tr class="even"><td><a href="/Document_object/documen2.md">document.addDataToSelection()</a></td><td>Stores specified data with the selected objects.</td></tr><tr class="odd"><td><a href="/Document_object/documen3.md">document.addFilter()</a></td><td>Applies a filter to the selected objects.</td></tr><tr class="even"><td><a href="/Document_object/documen4.md">document.addItem()</a></td><td>Adds an item from any open document or library to the specified Document object.</td></tr><tr class="odd"><td><a href="/Document_object/documen5.md">document.addNewLine()</a></td><td>Adds a new path between two points.</td></tr><tr class="even"><td><a href="/Document_object/documen6.md">document.addNewOval()</a></td><td>Adds a new Oval object in the specified bounding rectangle.</td></tr><tr class="odd"><td><a href="/Document_object/documen7.md">document.addNewPrimitiveOval()</a></td><td>Adds a new oval primitive fitting into the specified bounds.</td></tr><tr class="even"><td><a href="/Document_object/documen8.md">document.addNewPrimitiveRectangle()</a></td><td>Adds a new rectangle primitive fitting into the specified bounds.</td></tr><tr class="odd"><td><a href="/Document_object/documen9.md">document.addNewPublishProfile()</a></td><td>Adds a new publish profile and makes it the current one.</td></tr><tr class="even"><td><a href="/Document_object/docume10.md">document.addNewRectangle()</a></td><td>Adds a new rectangle or rounded rectangle, fitting it into the specified bounds.</td></tr><tr class="odd"><td><a href="/Document_object/docume11.md">document.addNewScene()</a></td><td>Adds a new scene (<a href="/Timeline_object/timeline_summary.md">Timeline object</a>) as the next scene after the currently selected scene and makes the new scene the currently selected scene.</td></tr><tr class="even"><td><a href="/Document_object/docume12.md">document.addNewText()</a></td><td>Inserts a new empty text field.</td></tr><tr class="even"><td><a href="/Document_object/docu6058.md">document.addTaggedSwatch()</a></td><td>To add new tagged swatch.</td></tr><tr class="odd"><td><a href="/Document_object/docu6059.md">document.addTaggedSwatchWithColor()</a></td><td>To add new tagged swatch with the given color string.</td></tr><tr class="odd"><td><a href="/Document_object/docume13.md">document.align()</a></td><td>Aligns the selection.</td></tr><tr class="even"><td><a href="/Document_object/docume14.md">document.allowScreens() - dropped</a></td><td>Dropped in Adobe Animate.</td></tr><tr class="odd"><td><a href="/Document_object/docume15.md">document.arrange()</a></td><td>Arranges the selection on the Stage.</td></tr><tr class="even"><td><a href="/Document_object/docume24.md">document.breakApart()</a></td><td>Performs a break-apart operation on the current selection.</td></tr><tr class="odd"><td><a href="/Document_object/docume25.md">document.canEditSymbol()</a></td><td>Indicates whether the Edit Symbols menu and functionality are enabled.</td></tr><tr class="even"><td><a href="/Document_object/docume26.md">document.canRevert()</a></td><td><p>Determines whether you can use the <a href="/Document_object/docum340.md">document.revert()</aor</p><p><a href="/flash_object_(fl)/fl61.md">fl.revertDocument()</amethod successfully.</p></td></tr></tbody></table>

<table><thead><tr class="header"><th><strong>Method</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/Document_object/docume27.md">document.canTestMovie()</a></td><td><p>Determines whether you can use the</p><p><a href="/Document_object/docu5948.md">document.testMovie()</amethod successfully.</p></td></tr><tr class="even"><td><a href="/Document_object/docume28.md">document.canTestScene()</a></td><td><p>Determines whether you can use the</p><p><a href="/Document_object/docu5979.md">document.testScene()</amethod successfully.</p></td></tr><tr class="odd"><td><a href="/Document_object/docume29.md">document.changeFilterOrder()</a></td><td>Changes the index of the filter in the Filters list.</td></tr><tr class="even"><td><a href="/Document_object/docume30.md">document.clipCopy()</a></td><td>Copies the current selection from the document to the Clipboard.</td></tr><tr class="odd"><td><a href="/Document_object/docume31.md">document.clipCut()</a></td><td>Cuts the current selection from the document and writes it to the Clipboard.</td></tr><tr class="even"><td><a href="/Document_object/docume32.md">document.clipPaste()</a></td><td>Pastes the contents of the Clipboard into the document.</td></tr><tr class="odd"><td><a href="/Document_object/docume33.md">document.close()</a></td><td>Closes the specified document.</td></tr><tr class="even"><td><a href="/Document_object/docume34.md">document.convertLinesToFills()</a></td><td>Converts lines to fills on the selected objects.</td></tr><tr class="odd"><td><a href="/Document_object/docume35.md">document.convertSelectionToBitmap()</a></td><td>Converts selected objects in the current frame to a bitmap and inserts the bitmap into the library.</td></tr><tr class="odd"><td><a href="/Document_object/docu6069.md">document.convertToDoc()</a></td><td>Converts a document to expected document type.</td></tr><tr class="even"><td><a href="/Document_object/docume36.md">document.convertToSymbol()</a></td><td>Converts the selected Stage items to a new symbol.</td></tr><tr class="odd"><td><a href="/Document_object/docume37.md">document.crop()</a></td><td>Uses the top selected drawing object to crop all selected drawing objects underneath it.</td></tr><tr class="even"><td><a href="/Document_object/docume40.md">document.debugMovie()</a></td><td>Initiates a debug session with the document.</td></tr><tr class="odd"><td><a href="/Document_object/docume41.md">document.deleteEnvelope()</a></td><td>Deletes the envelope (bounding box that contains one or more objects) from the selected object.</td></tr><tr class="even"><td><a href="/Document_object/docume42.md">document.deletePublishProfile()</a></td><td>Deletes the currently active profile, if there is more than one.</td></tr><tr class="odd"><td><a href="/Document_object/docume43.md">document.deleteScene()</a></td><td>Deletes the current scene (<a href="/Timeline_object/timeline_summary.md">Timeline object</a>), and if the deleted scene was not the last one, sets the next scene as the current Timeline object.</td></tr><tr class="even"><td><a href="/Document_object/docume44.md">document.deleteSelection()</a></td><td>Deletes the current selection on the Stage.</td></tr><tr class="odd"><td><a href="/Document_object/docu6065.md">document.deleteTaggedSwatchAtIndex()</a></td><td>Deletes tagged swatch with given index.</td></tr><tr class="even"><td><a href="/Document_object/docu6066.md">document.deleteTaggedSwatchByName()</a></td><td>Deletes tagged swatch with given name.</td></tr><tr class="odd"><td><a href="/Document_object/docume46.md">document.disableAllFilters()</a></td><td>Disables all filters on the selected objects.</td></tr><tr class="even"><td><a href="/Document_object/docume47.md">document.disableFilter()</a></td><td>Disables the specified filter in the Filters list.</td></tr><tr class="odd"><td><a href="/Document_object/docume48.md">document.disableOtherFilters()</a></td><td>Disables all filters except the one at the specified position in the Filters list.</td></tr><tr class="even"><td><a href="/Document_object/docume49.md">document.distribute()</a></td><td>Distributes the selection.</td></tr><tr class="odd"><td><a href="/Document_object/docume50.md">document.distributeToKeyframes()</a></td><td>Performs a distribute-to-keyframes operation on the current selection; equivalent to selecting Distriute to Keyframes.</td></tr><tr class="even"><td><a href="/Document_object/docume51.md">document.distributeToLayers()</a></td><td>Performs a distribute-to-layers operation on the current selection; equivalent to selecting Distribute to Layers.</td></tr><tr class="odd"><td><a href="/Document_object/docume53.md">document.documentHasData()</a></td><td>Checks the document for persistent data with the specified name.</td></tr><tr class="even"><td><a href="/Document_object/docume54.md">document.duplicatePublishProfile()</a></td><td>Duplicates the currently active profile and gives the duplicate version focus.</td></tr><tr class="odd"><td><a href="/Document_object/docume55.md">document.duplicateScene()</a></td><td>Makes a copy of the currently selected scene, giving the new scene a unique name and making it the current scene.</td></tr><tr class="even"><td><a href="/Document_object/docume56.md">document.duplicateSelection()</a></td><td>Duplicates the selection on the Stage.</td></tr></tbody></table>

<table><thead><tr class="header"><th><strong>Method</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/Document_object/docume57.md">document.editScene()</a></td><td>Makes the specified scene the currently selected scene for editing.</td></tr><tr class="even"><td><a href="/Document_object/docume58.md">document.enableAllFilters()</a></td><td>Enables all the filters on the Filters list for the selected objects.</td></tr><tr class="odd"><td><a href="/Document_object/docume59.md">document.enableFilter()</a></td><td>Enables the specified filter for the selected objects.</td></tr><tr class="even"><td><a href="/Document_object/docume60.md">document.enterEditMode()</a></td><td>Switches the authoring tool into the editing mode specified by the parameter.</td></tr><tr class="odd"><td><a href="/Document_object/docume61.md">document.exitEditMode()</a></td><td>Exits from symbol-editing mode and returns focus to the next level up from the editing mode.</td></tr><tr class="even"><td><a href="/Document_object/docu6070.md">document.exportCanvasPublishTemplate()</a></td><td>Exports the HTML5 Canvas Publishing Template for given document,at the specified location.</td></tr><tr class="even"><td><a href="/Document_object/docume62.md">document.exportInstanceToLibrary()</a></td><td>Export a selected movie clip, graphic, or button instance on the Stage to a new bitmap in the Library.</td></tr><tr class="odd"><td><p><a href="/Document_object/docume63.md">document.exportInstanceToPNGSequence(</a></p><p><a href="/Document_object/docume63.md">)</a></p></td><td>Export a selected movie clip, graphic, or button instance on the Stage to a series of PNG files on disk.</td></tr><tr class="even"><td><a href="/Document_object/docu6072.md">document.exportMedia()</a></td><td>Generates the required media from the document.</td></tr><tr class="even"><td><a href="/Document_object/docume64.md">document.exportPNG()</a></td><td>Exports the document as one or more PNG files.</td></tr><tr class="odd"><td><a href="/Document_object/docume65.md">document.exportPublishProfile()</a></td><td>Exports the currently active profile to an XML file.</td></tr><tr class="even"><td><a href="/Document_object/docume66.md">document.exportPublishProfileString()</a></td><td>Returns a string that specifies, in XML format, the specified profile.</td></tr><tr class="even"><td><a href="/Document_object/docu6074.md">document.exportSVG()</a></td><td>Exports the document in SVG format.</td></tr><tr class="odd"><td><a href="/Document_object/docume67.md">document.exportSWF()</a></td><td>Exports the document in the Flash SWF format.</td></tr><tr class="even"><td><a href="/Document_object/docume68.md">document.exportVideo()</a></td><td>Exports a video from the document and optionally sends it to Adobe Media Encoder to convert the video.</td></tr><tr class="odd"><td><a href="/Document_object/docume72.md">document.getAlignToDocument()</a></td><td>Identical to retrieving the value of the To Stage button in the Align panel.</td></tr><tr class="even"><td><a href="/Document_object/docume73.md">document.getBlendMode()</a></td><td>Returns a string that specifies the blending mode for the selected objects.</td></tr><tr class="odd"><td><a href="/Document_object/docume74.md">document.getCustomFill()</a></td><td>Retrieves the fill object of the selected shape, or the Tools panel and Property inspector if specified.</td></tr><tr class="even"><td><a href="/Document_object/docume75.md">document.getCustomStroke()</a></td><td>Returns the stroke object of the selected shape, or the Tools panel and Property inspector if specified.</td></tr><tr class="odd"><td><a href="/Document_object/docume76.md">document.getDataFromDocument()</a></td><td>Retrieves the value of the specified data.</td></tr><tr class="even"><td><a href="/Document_object/docume77.md">document.getElementProperty()</a></td><td>Gets the specified Element property for the current selection.</td></tr><tr class="odd"><td><a href="/Document_object/docume78.md">document.getElementTextAttr()</a></td><td>Gets a specified TextAttrs property of the selected Text objects.</td></tr><tr class="even"><td><a href="/Document_object/docume79.md">document.getFilters()</a></td><td>Returns an array that contains the list of filters applied to the currently selected objects.</td></tr><tr class="even"><td><a href="/Document_object/docu6060.md">document.getIndexForTaggedSwatchesPalette()</a></td><td>To get the Tagged Swatches palette index for given palette name.</td></tr><tr class="odd"><td><a href="/Document_object/docume80.md">document.getMetadata()</a></td><td>Returns a string containing the XML metadata associated with the document.</td></tr><tr class="even"><td><a href="/Document_object/docume81.md">document.getMobileSettings()</a></td><td><p>Returns the string passed to</p><p>document.setMobileSettings().</p></td></tr><tr class="odd"><td><a href="/Document_object/docume82.md">document.getPlayerVersion()</a></td><td>Returns a string that represents the targeted player version for the specified document.</td></tr><tr class="even"><td><a href="/Document_object/docume83.md">document.getPublishDocumentData()</a></td><td>Indicates whether publishing of the specified persistent data is enabled for the specified format in the document.</td></tr><tr class="odd"><td><a href="/Document_object/docume84.md">document.getSelectionRect()</a></td><td>Gets the bounding rectangle of the current selection.</td></tr></tbody></table>

| **Method**                                             | **Description**                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [document.getSWFPathFromProfile()](/Document_object/docume85.md)      | Gets the full path to the SWF file that is set in the current Publish profile.      
| [document.getTaggedSwatchAtIndex()](/Document_object/docu6061.md)      | Returns the Tagged Swatch with the given index.                                                                            |
| [document.getTaggedSwatchByName()](/Document_object/docu6062.md)      | Returns the Tagged Swatch with the given name.                                                                  |
| [document.getTaggedSwatches()](/Document_object/docu6064.md)      | Returns array of tagged swatch objects.                                                             |
| [document.getTaggedSwatchesPaletteList()](/Document_object/docu6063.md)      | To get the array of Tagged Swatches palette name list.                                                     |
| [document.getTelemetryForSwf()](/Document_object/docume86.md)         | Indicates whether the "Enable detailed telemetry" checkbox is selected in the Publish Settings dialog.                                                                           |
| [document.getTextString()](/Document_object/docume87.md)              | Gets the currently selected text.                                                                                                                                                |
| [document.getTimeline()](/Document_object/docume88.md)                | Retrieves the current [Timeline object](/Timeline_object/timeline_summary.md) in the document.                                                                                                         |
| [document.getTransformationPoint()](/Document_object/docume89.md)     | Gets the location of the transformation point of the current selection.                                                                                                          |
| [document.group()](/Document_object/docume90.md)                      | Converts the current selection to a group.     
 |
| [document.importCanvasPublishTemplate()](/Document_object/docu6071.md)                      | Imports and sets the HTML5 Canvas Publishing Template for given document, from the specified location pathURI.                                                                                                                                 |
| [document.importFile()](/Document_object/docume93.md)                 | Imports a file into the document.                                                                                                                                                |
| [document.importPublishProfile()](/Document_object/docume94.md)       | Imports a profile from a file.                                                                                                                                                   |
| [document.importPublishProfileString()](/Document_object/docume95.md) | Imports an XML string that represents a publish profile and sets it as the current profile.                                                                                      |
| [document.importSWF() - dropped](/Document_object/docume96.md)        | Dropped in Adobe Animate.                                                                                                                                                 |
| [document.intersect()](/Document_object/docume97.md)                  | Creates an intersection drawing object from all selected drawing objects.                                                                                                        |
| [document.loadCuepointXML() - dropped](/Document_object/docum110.md)  | Dropped in Adobe Animate.                                                                                                                                                        |
| [document.match()](/Document_object/docum120.md)                      | Makes the size of the selected objects the same.                                                                                                                                 |
| [document.mouseClick()](/Document_object/docum130.md)                 | Performs a mouse click from the Selection tool.                                                                                                                                  |
| [document.mouseDblClk()](/Document_object/docum140.md)                | Performs a double mouse click from the Selection tool.                                                                                                                           |
| [document.moveSelectedBezierPointsBy()](/Document_object/docum150.md) | If the selection contains at least one path with at least one Bézier point selected, this method moves all selected Bézier points on all selected paths by the specified amount. |
| [document.moveSelectionBy()](/Document_object/docum160.md)            | Moves selected objects by a specified distance.                                                                                                                                  |
| [document.optimizeCurves()](/Document_object/docum180.md)             | Optimizes smoothing for the current selection, allowing multiple passes, if specified, for optimal smoothing; equivalent to selecting Modify >Shape >Optimize.               |
| [document.publish()](/Document_object/docum210.md)                    | Publishes the document according to the active publish settings (File >Publish Settings); equivalent to selecting File >Publish.                                             |
| [document.punch()](/Document_object/docum230.md)                      | Uses the top selected drawing object to punch through all selected drawing objects underneath it.                                                                                |
| [document.removeAllFilters()](/Document_object/docum240.md)           | Removes all filters from the selected objects.                                                                                                                                   |
| [document.removeDataFromDocument()](/Document_object/docum250.md)     | Removes persistent data with the specified name that has been attached to the document.                                                                                          |
| [document.removeDataFromSelection()](/Document_object/docum260.md)    | Removes persistent data with the specified name that has been attached to the selection.                                                                                         |
| [document.removeFilter()](/Document_object/docum270.md)               | Removes the specified filter from the Filters list of the selected objects.                                                                                                      |
| [document.renamePublishProfile()](/Document_object/docum280.md)       | Renames the current profile.                                                                                                                                                     |
| [document.renameScene()](/Document_object/docum290.md)                | Renames the currently selected scene in the Scenes panel.                                                                                                                        |

| **Method**                                           | **Description**                                                                                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [document.reorderScene()](/Document_object/docum300.md)             | Moves the specified scene before another specified scene.                                                                                                                                                                                                           |
| [document.resetOvalObject()](/Document_object/docum310.md)          | Sets all values in the Property inspector to default Oval object settings.                                                                                                                                                                                          |
| [document.resetRectangleObject()](/Document_object/docum320.md)     | Sets all values in the Property inspector to default Rectangle object settings.                                                                                                                                                                                     |
| [document.resetTransformation()](/Document_object/docum330.md)      | Resets the transformation matrix; equivalent to selecting Modify >Transform >Remove Transform.                                                                                                                                                                  |
| [document.revert()](/Document_object/docum340.md)                   | Reverts the specified document to its previously saved version; equivalent to selecting File >Revert.                                                                                                                                                             |
| [document.rotate3DSelection()](/Document_object/docum350.md)        | Applies a 3D rotation to the selection.                                                                                                                                                                                                                             |
| [document.rotateSelection()](/Document_object/docum360.md)          | Rotates the selection by a specified number of degrees.                                                                                                                                                                                                             |
| [document.save()](/Document_object/docum370.md)                     | Saves the document in its default location; equivalent to selecting File >Save.                                                                                                                                                                                   |
| [document.saveAsCopy()](/Document_object/docum390.md)               | Saves a copy of the document to a specified location.                                                                                                                                                                                                               |
| [document.saveAndCompact() - dropped](/Document_object/docum380.md) | Dropped in Adobe Animate.                                                                                                                                                                                                     |
| [document.scaleSelection()](/Document_object/docum400.md)           | Scales the selection by a specified amount; equivalent to using the Free Transform tool to scale the object.                                                                                                                                                        |
| [document.selectAll()](/Document_object/docum420.md)                | Selects all items on the Stage; equivalent to pressing Control+A (Windows) or Command+A (Macintosh) or selecting Edit >Select All.                                                                                                                                |
| [document.selectNone()](/Document_object/docum440.md)               | Deselects any selected items.                                                                                                                                                                                                                                       |
| [document.setAlignToDocument()](/Document_object/docum450.md)       | Sets the preferences for [document.align()](/Document_object/docume13.md), [document.distribute()](/Document_object/docume49.md), [document.match()](/Document_object/docum120.md), and [document.space()](/Document_object/docum67.md) to act on the document; equivalent to enabling the To Stage button in the Align panel. |
| [document.setBlendMode()](/Document_object/docum460.md)             | Sets the blending mode for the selected objects.                                                                                                                                                                                                                    |
| [document.setCustomFill()](/Document_object/docum470.md)            | Sets the fill settings for the Tools panel, Property inspector, and any selected shapes.                                                                                                                                                                            |
| [document.setCustomStroke()](/Document_object/docum480.md)          | Sets the stroke settings for the Tools panel, Property inspector, and any selected shapes.                                                                                                                                                                          |
| [document.setElementProperty()](/Document_object/docum490.md)       | Sets the specified Element property on selected objects in the document.                                                                                                                                                                                            |
| [document.setElementTextAttr()](/Document_object/docum500.md)       | Sets the specified TextAttrs property of the selected text items to the specified value.                                                                                                                                                                            |
| [document.setFillColor()](/Document_object/docum510.md)             | Changes the selection and the tools panel to the specified color.                                                                                                                                                                                                   |
| [document.setFilterProperty()](/Document_object/docum520.md)        | Sets a specified filter property for the currently selected objects.                                                                                                                                                                                                |
| [document.setFilters()](/Document_object/docum530.md)               | Applies filters to the selected objects.                                                                                                                                                                                                                            |
| [document.setInstanceAlpha()](/Document_object/docum540.md)         | Sets the opacity of the instance.                                                                                                                                                                                                                                   |
| [document.setInstanceBrightness()](/Document_object/docum550.md)    | Sets the brightness for the instance.                                                                                                                                                                                                                               |
| [document.setInstanceTint()](/Document_object/docum560.md)          | Sets the tint for the instance.                                                                                                                                                                                                                                     |

| **Method**                                             | **Description**                                                                                                                         |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [document.setMetadata()](/Document_object/docum570.md)                | Sets the XML metadata for the specified document, overwriting any existing metadata.                                                    |
| [document.setMobileSettings()](/Document_object/docum580.md)          | Sets the value of an XML settings string in a mobile FLA file.                                                             |
| [document.setOvalObjectProperty()](/Document_object/docum590.md)      | Specifies a value for a specified property of primitive Oval objects.                                                                   |
| [document.setPlayerVersion()](/Document_object/docum600.md)           | Sets the version of the Flash Player targeted by the specified document.                                                                |
| [document.setRectangleObjectProperty()](/Document_object/docu9643.md) | Specifies a value for a specified property of primitive Rectangle objects.                                                              |
| [document.setSelectionBounds()](/Document_object/docu9658.md)         | Moves and resizes the selection in a single operation.                                                                                  |
| [document.setSelectionRect()](/Document_object/docu9689.md)           | Draws a rectangular selection marquee relative to the Stage, using the specified coordinates.                                           |
| [document.setStageVanishingPoint()](/Document_object/docu9705.md)     | Specifies the vanishing point for viewing 3D objects.                                                                                   |
| [document.setStageViewAngle()](/Document_object/docu9721.md)          | Specifies the perspective angle for viewing 3D objects.                                                                                 |
| [document.setStroke()](/Document_object/docu9752.md)                  | Sets the color, width, and style of the selected strokes.                                                                               |
| [document.setStrokeColor()](/Document_object/docu9768.md)             | Changes the stroke color of the selection to the specified color.                                                                       |
| [document.setStrokeSize()](/Document_object/docu9799.md)              | Changes the stroke size of the selection to the specified size.                                                                         |
| [document.setStrokeStyle()](/Document_object/docu9814.md)             | Changes the stroke style of the selection to the specified style. 
|
| [document.setTaggedSwatchAtIndex()](/Document_object/docu6067.md)             | Replace the tagged swatch with the given index to the given new swatch object.  
|
| [document.setTaggedSwatchByName()](/Document_object/docu6068.md)             | Replace the tagged swatch with the given name to the given new swatch object                                                                                    |
| [document.setTextRectangle()](/Document_object/docu9846.md)           | Changes the bounding rectangle for the selected text item to the specified size.                                                        |
| [document.setTextSelection()](/Document_object/docu9861.md)           | Sets the text selection of the currently selected text field to the values specified by the ***startIndex*** and ***endIndex*** values. |
| [document.setTextString()](/Document_object/docu9908.md)              | Inserts a string of text.                                                                                                               |
| [document.setTransformationPoint()](/Document_object/docu9939.md)     | Moves the transformation point of the current selection.                                                                                |
| [document.skewSelection()](/Document_object/docum5.md)              | Skews the selection by a specified amount.                                                                                              |
| [document.smoothSelection()](/Document_object/docum21.md)            | Smooths the curve of each selected fill outline or curved line.                                                                         |
| [document.space()](/Document_object/docum67.md)                      | Spaces the objects in the selection evenly.                                                                                             |
| [document.straightenSelection()](/Document_object/docum83.md)        | Straightens the currently selected strokes; equivalent to using the Straighten button in the Tools panel.                               |
| [document.swapElement()](/Document_object/docum114.md)                | Swaps the current selection with the specified one.                                                                                     |
| [document.swapStrokeAndFill()](/Document_object/docu5901.md)          | Swaps the Stroke and Fill colors.                                                                                                       |
| [document.testMovie()](/Document_object/docu5948.md)                  | Executes a Test Movie operation on the document.                                                                                        |
| [document.testScene()](/Document_object/docu5979.md)                  | Executes a Test Scene operation on the current scene of the document.                                                                   |
| [document.traceBitmap()](/Document_object/docu6010.md)                | Performs a trace bitmap on the current selection; equivalent to selecting Modify>Bitmap>Trace Bitmap.                             |
| [document.transformSelection()](/Document_object/docu6073.md)         | Performs a general transformation on the current selection by applying the matrix specified in the arguments.                           |
| [document.translate3DCenter()](/Document_object/docu6042.md)          | Sets the XYZ position around which the selection is translated or rotated.                                                              |

| **Method**                                       | **Description**                                              |
|--------------------------------------------------|--------------------------------------------------------------|
| [document.translate3DSelection()](/Document_object/docu6057.md) | Applies a 3D translation to the selection.                   |
| [document.unGroup()](/Document_object/docu6104.md)              | Ungroups the current selection.                              |
| [document.union()](/Document_object/docu6120.md)                | Combines all selected shapes into a drawing object.          |
| [document.unlockAllElements()](/Document_object/docu6135.md)    | Unlocks all locked elements on the currently selected frame. |
| [document.xmlPanel()](/Document_object/docu6198.md)             | Posts a XMLUI dialog box.                                    |

    
#### Property summary

You can use the following properties with the Document object.

| **Property**                                    | **Description**                                                                                                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [document.accName](/Document_object/document.md)           | A string that is equivalent to the Name field in the Accessibility panel.                                                                                                    |
| [document.as3AutoDeclare](/Document_object/docume16.md)        | A Boolean value that describes whether the instances placed on the Stage are automatically added to user-defined timeline classes.                                           |
| [document.as3Dialect](/Document_object/docume17.md)            | A string that describes the ActionScript 3.0 "dialect" being used in the specified document.                                                                                 |
| [document.as3ExportFrame](/Document_object/docume18.md)        | An integer that specifies in which frame to export ActionScript 3.0 classes.                                                                                                 |
| [document.as3StrictMode](/Document_object/docume19.md)         | A Boolean value that specifies whether the ActionScript 3.0 compiler should compile with the Strict Mode option turned on or off.                                            |
| [document.as3WarningsMode](/Document_object/docume20.md)       | A Boolean value that specifies whether the ActionScript 3.0 compiler should compile with the Warnings Mode option turned on or off.                                          |
| [document.asVersion](/Document_object/docume21.md)             | An integer that specifies which version of ActionScript is being used in the specified file.                                                                                 |
| [document.autoLabel](/Document_object/docume22.md)             | A Boolean value that is equivalent to the Auto Label check box in the Accessibility panel.                                                                                   |
| [document.backgroundColor](/Document_object/docume23.md)       | A string, hexadecimal value, or integer that represents the background color.                                                                                                |
| [document.currentPublishProfile](/Document_object/docume38.md) | A string that specifies the name of the active publish profile for the specified document.                                                                                   |
| [document.currentTimeline](/Document_object/docume39.md)       | An integer that specifies the index of the active timeline.                                                                                                                  |
| [document.description](/Document_object/docume45.md)           | A string that is equivalent to the Description field in the Accessibility panel.                                                                                             |
| [document.docClass](/Document_object/docume52.md)              | Specifies the top-level ActionScript 3.0 class associated with the document.                                                                                                 |
| [document.externalLibraryPath](/Document_object/docume69.md)   | A string that contains a list of items in the document’s ActionScript 3.0 External library path, which specifies the location of SWC files used as runtime shared libraries. |
| [document.forceSimple](/Document_object/docume70.md)           | A Boolean value that specifies whether the children of the specified object are accessible.                                                                                  |
| [document.frameRate](/Document_object/docume71.md)             | A float value that specifies the number of frames displayed per second when the SWF file plays; the default is 12.                                                           |
| [document.height](/Document_object/docume91.md)                | An integer that specifies the height of the document (Stage) in pixels.                                                                                                      |

| **Property**                                      | **Description**                                                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [document.id](/Document_object/docume92.md)                      | A unique integer (assigned automatically) that identifies a document during a Flash session.                                                                       |
| [document.library](/Document_object/docume98.md)                 | Read-only; the [library object](/library_object/library_summary.md) for a document.                                                                                                     |
| [document.libraryPath](/Document_object/docume99.md)             | A string that contains a list of items in the document’s ActionScript 3.0 Library path, which specifies the location of SWC files or folders containing SWC files. |
| [document.livePreview](/Document_object/docum100.md)             | A Boolean value that specifies whether Live Preview is enabled.                                                                                                    |
| [document.name](/Document_object/docum170.md)                    | Read-only; a string that represents the name of a document (FLA file).                                                                                             |
| [document.path](/Document_object/docum190.md)                    | Read-only; a string that represents the path of the document, in a platform-specific format.                                                                       |
| [document.pathURI](/Document_object/docum200.md)                 | Read-only; a string that represents the path of the document, expressed as a file:/// URI.                                                                         |
| [document.publishProfiles](/Document_object/docum220.md)         | Read-only; an array of the publish profile names for the document.                                                                                                 |
| [document.screenOutline - dropped](/Document_object/docum410.md) | Dropped in Adobe Animate.                                                                                                                                          |
| [document.selection](/Document_object/docum430.md)               | An array of the selected objects in the document.                                                                                                                  |
| [document.silent](/Document_object/docu9971.md)                  | A Boolean value that specifies whether the object is accessible.                                                                                                   |
| [document.sourcePath](/Document_object/docum36.md)              | A string that contains a list of items in the document’s ActionScript 3.0 Source path, which specifies the location of ActionScript class files.                   |
| [document.swfJPEGQuality](/Document_object/docu5932.md)          | An integer that returns the JPEG Quality setting from the current Publish Profile in the document.                                                                 |
| [document.timelines](/Document_object/docu5995.md)               | Read-only; an array of Timeline objects (see [Timeline object](/Timeline_object/timeline_summary.md)).                                                                                   |
| [document.viewMatrix](/Document_object/docu6167.md)              | Read-only; a [Matrix object](/Matrix_object/matrix_summary.md).                                                                                                                       |
| [document.width](/Document_object/docu6182.md)                   | An integer that specifies the width of the document (Stage) in pixels.                                                                                             |
| [document.zoomFactor](/Document_object/docu6229.md)              | Specifies the zoom percent of the Stage at authoring time.                                                                                                         |

<span id="document.accName" class="anchor"></span>


## drawingLayer


#### Availability

Flash MX 2004.

#### Description

The drawingLayer object is accessible from JavaScript as a child of the flash object. The drawingLayer object is used for extensible tools when the user wants to temporarily draw while dragging—for example, when creating a selection marquee. You should call [drawingLayer.beginFrame()](/drawingLayer_object/drawingLaye1.md) before you call any other drawingLayer methods.

#### Method summary

The following methods are available for the drawingLayer object:

| **Method**                                            | **Description**                                                                                                 |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [drawingLayer.beginDraw()](/drawingLayer_object/drawingLayer.md) | Puts Flash in drawing mode.                                                                                     |
| [drawingLayer.beginFrame()](/drawingLayer_object/drawingLaye1.md)            | Erases what was previously drawn using the drawingLayer and prepares for more drawing commands.                 |
| [drawingLayer.cubicCurveTo()](/drawingLayer_object/drawingLaye2.md)          | Draws a cubic curve from the current pen location using the parameters as the coordinates of the cubic segment. |
| [drawingLayer.curveTo()](/drawingLayer_object/drawingLaye3.md)               | Draws a quadratic curve segment starting at the current drawing position and ending at a specified point.       |
| [drawingLayer.drawPath()](/drawingLayer_object/drawingLaye4.md)              | Draws the specified path.                                                                                       |
| [drawingLayer.endDraw()](/drawingLayer_object/drawingLaye5.md)               | Exits drawing mode.                                                                                             |
| [drawingLayer.endFrame()](/drawingLayer_object/drawingLaye6.md)              | Signals the end of a group of drawing commands.                                                                 |
| [drawingLayer.lineTo()](/drawingLayer_object/drawingLaye7.md)                | Draws a line from the current drawing position to the point (*x,y*).                                            |
| [drawingLayer.moveTo()](/drawingLayer_object/drawingLaye8.md)                | Sets the current drawing position.                                                                              |
| [drawingLayer.newPath()](/drawingLayer_object/drawingLaye9.md)               | Returns a new [Path object](/Path_object/path_summary.md).                                                                     |
| [drawingLayer.setColor()](/drawingLayer_object/drawingLay10.md)              | Sets the color of subsequently drawn data.                                                                      |
| [drawingLayer.setFill()](/drawingLayer_object/drawingLay11.md)               | This method is not available.                                                                                   |
| [drawingLayer.setStroke()](/drawingLayer_object/drawingLay12.md)             | This method is not available.                                                                                   |

<span id="drawingLayer.beginDraw()" class="anchor"></span>



## edge Object


#### Availability

Flash MX 2004.

#### Description

The Edge object represents an edge of a shape on the Stage.

#### Method summary

The following methods are available for the Edge object:

| **Method**                          | **Description**                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------|
| [edge.getControl()](/Edge_object/edge1.md)  | Gets a point object set to the location of the specified control point of the edge. |
| [edge.getHalfEdge()](/Edge_object/edge2.md) | Returns a [HalfEdge object](/HalfEdge_object/halfEdge_summary.md).                                         |
| [edge.setControl()](/Edge_object/edge5.md)  | Sets the position of the control point of the edge.                                 |
| [edge.splitEdge()](/Edge_object/edge6.md)   | Splits the edge into two pieces.                                                    |

#### Property summary

The following properties are available for the Edge object:

| **Property**                                      | **Description**                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------|
| [edge.cubicSegmentIndex](/Edge_object/edge.md) | An integer that specifies the index value of a cubic segment of the edge. |
| [edge.id](/Edge_object/edge3.md)                          | Read-only; an integer that represents a unique identifier for the edge.   |
| [edge.isLine](/Edge_object/edge4.md)                      | Read-only; an integer with a value of 0 or 1.                             |
| [edge.stroke](/Edge_object/edge7.md)                      | A [Stroke object](/Stroke_object/stroke_summary.md).                                         |

<span id="edge.cubicSegmentIndex" class="anchor"></span>



## element Object

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


## fill Object


#### Availability

Flash MX 2004.

#### Description

This object contains all the properties of the Fill color setting of the Tools panel or of a selected shape. To retrieve a Fill object, use [document.getCustomFill()](/Document_object/docume74.md).

#### Property summary

The following properties are available for the Fill object:

| **Property**                                                            | **Description**                                                                                                           |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [fill.bitmapIsClipped](/Fill_object/fill.md) | A Boolean value that specifies whether the bitmap fill for a shape that is larger than the bitmap is clipped or repeated. |
| [fill.bitmapPath](/Fill_object/fill1.md)                                        | A string that specifies the path and name of the bitmap fill in the Library.                                              |
| [fill.color](/Fill_object/fill2.md)                                             | A string, hexadecimal value, or integer that represents the fill color.                                                   |
| [fill.colorArray](/Fill_object/fill3.md)                                        | An array of colors in gradient.                                                                                           |
| [fill.focalPoint](/Fill_object/fill4.md)                                        | An integer that specifies the gradient focal point horizontal offset from the transformation point.                       |
| [fill.linearRGB](/Fill_object/fill5.md)                                         | A Boolean value that specifies whether to render the fill as a linear or radial RGB gradient.                             |
| [fill.matrix](/Fill_object/fill6.md)                                            | A [Matrix object](/Matrix_object/matrix_summary.md) that defines the placement, orientation, and scales for gradient fills.                  |
| [fill.overflow](/Fill_object/fill7.md)                                          | A string that specifies the behavior of a gradient’s overflow.                                                            |
| [fill.posArray](/Fill_object/fill8.md)                                          | An array of integers, each in the range of zero to 255, indicating the position of the corresponding color.               |
| [fill.style](/Fill_object/fill9.md)                                             | A string that specifies the fill style.                                                                                   |

<span id="fill.bitmapIsClipped" class="anchor"></span>



## filter Object


#### Availability

Flash 8.

#### Description

This object contains all the properties for all filters. The filter.name property specifies the type of filter, and determines which properties are applicable to each filter. See [filter.name](/Filter_object/filter13.md).

To return the filter list for an object or objects, use document.getFilters(). To apply filters to an object or objects, use document.setFilters(). See [document.getFilters()](/Document_object/docume79.md) and [document.setFilters()](/Document_object/docum530.md).

#### Property summary

The following properties can be used with the Filter object:

| **Property**                           | **Description**                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [filter.angle](/Filter_object/filter.md)          | A float value that specifies the angle of the shadow or highlight color, in degrees.            |
| [filter.blurX](/Filter_object/filter1.md)          | A float value that specifies the amount to blur in the x direction, in pixels.                  |
| [filter.blurY](/Filter_object/filter2.md)          | A float value that specifies the amount to blur in the y direction.                             |
| [filter.brightness](/Filter_object/filter3.md)     | A float value that specifies the brightness of the filter.                                      |
| [filter.color](/Filter_object/filter4.md)          | A string, hexadecimal value, or integer that represents the filter color.                       |
| [filter.contrast](/Filter_object/filter5.md)       | A float value that specifies the contrast value of the filter.                                  |
| [filter.distance](/Filter_object/filter6.md)       | A float value that specifies the distance between the filter’s effect and an object, in pixels. |
| [filter.enabled](/Filter_object/filter7.md)        | A Boolean value that specifies whether the specified filter is enabled.                         |
| [filter.hideObject](/Filter_object/filter8.md)     | A Boolean value that specifies whether the source image is hidden.                              |
| [filter.highlightColor](/Filter_object/filter9.md) | A string, hexadecimal value, or integer that represents the highlight color.                    |
| [filter.hue](/Filter_object/filter10.md)            | A float value that specifies the hue of the filter.                                             |
| [filter.inner](/Filter_object/filter11.md)          | A Boolean value that specifies whether the shadow is an inner shadow.                           |
| [filter.knockout](/Filter_object/filter12.md)       | A Boolean value that specifies whether the filter is a knockout filter.                         |
| [filter.name](/Filter_object/filter13.md)           | Read-only; a string that specifies the type of filter.                                          |
| [filter.quality](/Filter_object/filter14.md)        | A string that specifies the blur quality.                                                       |
| [filter.saturation](/Filter_object/filter15.md)     | A float value that specifies the saturation value of the filter.                                |
| [filter.shadowColor](/Filter_object/filter16.md)    | A string, hexadecimal value, or integer that represents the shadow color.                       |
| [filter.strength](/Filter_object/filter17.md)       | An integer that specifies the percentage strength of the filter.                                |
| [filter.type](/Filter_object/filter18.md)           | A string that specifies the type of bevel or glow.                                              |

<span id="filter.angle" class="anchor"></span>



## flash(fl.()) Object



#### Availability

Flash MX 2004.

#### Description

The flash object represents the Flash application. You can use flash or fl to refer to this object. This documentation uses fl in code samples throughout.

#### Method summary

The following methods can be used with the flash object:

| **Method**                                       | **Description**                                                                                                |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [fl.addEventListener()](/flash_object_(fl)/fl1.md)           | Registers a function to be called when a specific event is received.                                           |
| [fl.addToolInToolbar()](/flash_object_(fl)/fl1.md)           | Add the specified tool from master toolbar to main toolbar, appends in the last.                                           |
| [fl.browseForFileURL()](/flash_object_(fl)/fl3.md)           | Opens a File Open or File Save system dialog box and lets the user specify a file to be opened or saved.       |
| [fl.browseForFolderURL()](/flash_object_(fl)/fl4.md)         | Displays a Browse for Folder dialog box and lets the user select a folder.                                     |
| [fl.clearPublishCache()](/flash_object_(fl)/fl5.md)          | Clears the publish cache.                                                                                      |
| [fl.clipCopyString()](/flash_object_(fl)/fl6.md)             | Copies the specified string to the Clipboard.                                                                  |
| [fl.closeAll()](/flash_object_(fl)/fl7.md)                   | Closes all open documents, displaying the Save As dialog box for any documents that were not previously saved. |
| [fl.closeAllPlayerDocuments()](/flash_object_(fl)/fl8.md)    | Closes all the SWF files that were opened with Control > Test Movie.                                          |
| [fl.closeDocument()](/flash_object_(fl)/fl9.md)              | Closes the specified document.                                                                                 |
| [fl.copyLibraryItem()](/flash_object_(fl)/fl15.md)            | Silently copies a library item from a document without exposing the item in the Flash Pro user interface.      |
| [fl.createDocument()](/flash_object_(fl)/fl16.md)             | Opens a new document and selects it.                                                                           |
| [fl.exportPublishProfileString()](/flash_object_(fl)/fl22.md) | Uniform Resource Identifier (URI) from which to export publish settings.                                       |
| [fl.fileExists()](/flash_object_(fl)/fl24.md)                 | Checks whether a file already exists on disk.                                                                  |
| [fl.findDocumentDOM()](/flash_object_(fl)/fl25.md)            | Lets you target a specific file by using its unique identifier.                                                |
| [fl.findDocumentIndex()](/flash_object_(fl)/fl26.md)          | Returns an array of integers that represent the position of a document in the fl.documents array.              |
| [fl.findObjectInDocByName()](/flash_object_(fl)/fl27.md)      | Exposes elements with instance names that match specified text.                                                |
| [fl.findObjectInDocByType()](/flash_object_(fl)/fl28.md)      | Exposes elements of a specified element type in a document.                                                    |
| [fl.getAppMemoryInfo()](/flash_object_(fl)/fl30.md)           | Returns an integer that represents the number of bytes being used in a specified area of Flash.exe memory.     |
| [fl.getDocumentDOM()](/flash_object_(fl)/fl31.md)             | Retrieves the DOM ([Document object](/Document_object/document_summary.md)) of the currently active document.                         |

<table><thead><tr class="header"><th><strong>Method</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/flash_object_(fl)/fl35.md">fl.getSwfPanel()</a></td><td>Returns the SWFPanel object based on the panel's localized name or its SWF filename.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl32.md">fl.getThemeColor()</a></td><td>Retrieves a theme color that matches the parameter specified theme parameter name.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl33.md">fl.getThemeColorParameters()</a></td><td>Retrieves an array of theme parameter names.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl34.md">fl.getThemeFontInfo()</a></td><td>Return either the font style or the font size that is used to draw the UI of the specified size.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl37.md">fl.isFontInstalled()</a></td><td>Determines whether a specified font is installed.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl40.md">fl.mapPlayerURL()</a></td><td>Maps an escaped Unicode URL to a UTF-8 or MBCS URL.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl45.md">fl.openDocument()</a></td><td>Opens a Flash (FLA) document for editing in a new Flash Document window and gives it focus.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl46.md">fl.openScript()</a></td><td>Opens a script (JSFL, AS, ASC) or other file (XML, TXT) in the Flash text editor.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl55.md">fl.quit()</a></td><td>Quits Flash, prompting the user to save any changed documents.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl56.md">fl.reloadEffects() - dropped</a></td><td>Dropped in Adobe Animate.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl57.md">fl.reloadTools()</a></td><td>Rebuilds the Tools panel from the toolconfig.xml file.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl58.md">fl.removeEventListener()</a></td><td><p>Unregisters a function that was registered using</p><p>fl.addEventListener().</p></td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl59.md">fl.resetAS3PackagePaths()</a></td><td>Resets the global Classpath setting in the ActionScript 3.0 Settings dialog box to the default value.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl60.md">fl.resetPackagePaths() - dropped</a></td><td>Dropped in Adobe Animate.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl62.md">fl.runScript()</a></td><td>Executes a JavaScript file.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl63.md">fl.saveAll()</a></td><td>Saves all open documents, displaying the Save As dialog box for any documents that were not previously saved.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl64.md">fl.saveDocument()</a></td><td>Saves the specified document as a FLA document.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl65.md">fl.saveDocumentAs()</a></td><td>Displays the Save As dialog box for the specified document.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl67.md">fl.selectElement()</a></td><td>Enables selection or editing of an element.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl68.md">fl.selectTool()</a></td><td>Selects the specified tool in the Tools panel.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl69.md">fl.setActiveWindow()</a></td><td>Sets the active window to be the specified document.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl71.md">fl.setPrefBoolean()</a></td><td>Sets a boolean preference value.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl70.md">fl.showIdleMessage()</a></td><td>Lets you disable the warning about a script running too long.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl75.md">fl.toggleBreakpoint()</a></td><td>Toggles a breakpoint for the given .as file at the given line.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl77.md">fl.trace()</a></td><td>Sends a text string to the Output panel.</td></tr><tr class="even"><td><a href="/flash_object_(fl)/fl79.md">fl.xmlPanel()</a></td><td>Launches the XML To UI dialog from a URI that points to an XML-format file.</td></tr><tr class="odd"><td><a href="/flash_object_(fl)/fl80.md">fl.xmlPanelFromString()</a></td><td>Launches the XML To UI dialog from an XML-format string.</td></tr></tbody></table>

#### Property summary

The following properties can be used with the flash object.

| **Property**                                                           | **Description**                                                                                                                                                          |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [fl.actionsPanel](/flash_object_(fl)/fl.md)                                    | Read-only; an [actionsPanel object](/actionsPanel_object/actionsPanel_summary.md).                                                                                                                       |
| [fl.as3PackagePaths](/flash_object_(fl)/fl2.md)                                    | A string that corresponds to the global Classpath setting in the ActionScript 3.0 Settings dialog box.                                                                   |
| [fl.compilerErrors](/flash_object_(fl)/fl10.md)                                     | Read-only; a [compilerErrors object](/compilerErrors_object/compilerErrors_summary.md).                                                                                                                      |
| [fl.componentsPanel](/flash_object_(fl)/fl11.md)                                    | Read-only; a [componentsPanel object](/componentsPanel_object/componentsPanel_summary.md), which represents the Components panel.                                                                             |
| [fl.configDirectory](/flash_object_(fl)/fl12.md)                                    | Read-only; a string that specifies the full path for the local user’s Configuration folder as a platform-specific path.                                                  |
| [fl.configURI](/flash_object_(fl)/fl13.md)                                          | Read-only; a string that specifies the full path for the local user’s Configuration directory as a file:/// URI.                                                         |
| [fl.contactSensitiveSelection](/flash_object_(fl)/fl14.md)                          | A Boolean value that specifies whether Contact Sensitive selection mode is enabled.                                                                                      |
| [fl.createNewDocList](/flash_object_(fl)/fl17.md)                                   | Read-only; an array of strings that represent the various types of documents that can be created.                                                                        |
| [fl.createNewDocListType](/flash_object_(fl)/fl18.md)                               | Read-only; an array of strings that represent the file extensions of the types of documents that can be created.                                                         |
| [fl.createNewTemplateList](/flash_object_(fl)/fl19.md)                              | Read-only; an array of strings that represent the various types of templates that can be created.                                                                        |
| [fl.documents](/flash_object_(fl)/fl20.md)                                          | Read-only; an array of Document objects (see [Document object](/Document_object/document_summary.md)) that represent the documents (FLA files) that are currently open for editing.             |
| [fl.drawingLayer](/flash_object_(fl)/fl21.md)                                       | The drawingLayer object that an extensible tool should use when the user wants to temporarily draw while dragging.                                                       |
| [fl.externalLibraryPath](/flash_object_(fl)/fl23.md)                                | A string that contains a list of items in the global ActionScript 3.0 External library path, which specifies the location of SWC files used as runtime shared libraries. |
| [fl.flexSDKPath](/flash_object_(fl)/fl29.md)                                        | A string that specifies the path to the Flex SDK folder, which contains bin, frameworks, lib, and other folders.                                                         |
| [fl.installedPlayers](/flash_object_(fl)/fl36.md)                                   | Returns an array of generic objects corresponding to the list of installed Flash Players in the document Property inspector.                                             |
| [fl.languageCode](/flash_object_(fl)/fl38.md)                                       | Returns the five character code identifying the locale of the application’s user interface.                                                                              |
| [fl.libraryPath](/flash_object_(fl)/fl39.md)                                        | A string that contains a list of items in the global ActionScript 3.0 Library path, which specifies the location of SWC files or folders containing SWC files.           |
| [fl.Math](/flash_object_(fl)/fl41.md)                                               | Read-only; the [Math object](/Math_object/Math_summary.md), which provides methods for matrix and point operations.                                                                     |
| [fl.mruRecentFileList](/flash_object_(fl)/fl42.md)                                  | Read-only; an array of the complete filenames in the Most Recently Used (MRU) list that the Flash authoring tool manages.                                                |
| [fl.mruRecentFileListType](/flash_object_(fl)/fl43.md)                              | Read-only; an array of the file types in the MRU list that the Flash authoring tool manages.                                                                             |
| [fl.packagePaths - dropped](/flash_object_(fl)/fl48.md)                             | Dropped in Adobe Animate.                                                                                                                                                |
| [fl.publishCacheDiskSizeMax](/flash_object_(fl)/fl50.md)                            | An integer that sets the disk cache size limit preference.                                                                                                               |
| [fl.publishCacheEnabled](/flash_object_(fl)/fl51.md)                                | A boolean value that sets whether publish cache is enabled.                                                                                                              |
| [fl.publishCacheMemoryEntrySizeLimit](/flash_object_(fl)/fl52.md) | An integer property that sets the maximum size for the memory cache entry preference.                                                                                    |

| **Property**                                  | **Description**                                                                                                                              |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [fl.publishCacheMemorySizeMax](/flash_object_(fl)/fl53.md) | An integer that sets the memory cache size limit preference.                                                                                 |
| [fl.objectDrawingMode](/flash_object_(fl)/fl44.md)         | An integer that represents the object drawing mode that is enabled.                                                                          |
| [fl.outputPanel](/flash_object_(fl)/fl47.md)               | Read-only; reference to the [outputPanel object](/outputPanel_object/outputPanel_summary.md).                                                                             |
| [fl.presetPanel](/flash_object_(fl)/fl49.md)               | Read-only; a [presetPanel object](/presetPanel_object/presetPanel_summary.md).                                                                                            |
| [fl.scriptURI](/flash_object_(fl)/fl66.md)                 | Read-only; a string that represents the path of the currently running JSFL script, expressed as a file:/// URI.                              |
| [fl.sourcePath](/flash_object_(fl)/fl72.md)                | A string that contains a list of items in the global ActionScript 3.0 Source path, which specifies the location of ActionScript class files. |
| [fl.spriteSheetExporter](/flash_object_(fl)/fl73.md)       | Returns an instance of SpriteSheetExporter object.                                                                                           |
| [fl.swfPanels](/flash_object_(fl)/fl74.md)                 | An array of registered swfPanel objects (see [swfPanel object](/swfPanel_object/swfPanel_summary.md)).                                                              |
| [fl.tools](/flash_object_(fl)/fl76.md)                     | Read-only; an array of Tools objects.                                                                                                        |
| [fl.version](/flash_object_(fl)/fl78.md)                   | Read-only; the long string version of the Flash authoring tool, including platform.                                                          |
| [fl.xmlui](/flash_object_(fl)/fl81.md)                     | Read-only; an [XMLUI object](/XMLUI_object/xmlui_summary.md).                                                                                                |

<span id="fl.actionsPanel" class="anchor"></span>



## FLfile Object



#### Availability

Flash MX 2004 7.2.

#### Description

The FLfile object lets you write Flash extensions that can access, modify, and remove files and folders on the local file system. The FLfile API is provided in the form of an extension to the JavaScript API. This extension is called a *shared library* and is located in the following folder:

-   Windows 7 and 8:

*boot drive*\\Users\\*username*\\AppData\\Local\\Adobe\\Flash CC\\*language*\\Configuration\\External Libraries\\FLfile.dll

-   Mac OS X:

Macintosh HD/Users/*username*/Library/Application Support/Adobe/Flash CC/*language*/Configuration/External Libraries/FLfile.dll

***Note:** Don't confuse the shared libraries that contain symbols in your Flash documents with the JavaScript API shared libraries. They are two different things.*

The FLfile methods work with files or folders (directories) on disk. Therefore, each method takes one or more parameters to specify the location of a file or folder. The location of the file or folder is expressed as a string in a form very similar to a website URL. It is called a file URI (Uniform Resource Identifier) and is formatted as shown here (including the quote marks):

*"file:///drive\|/folder 1/folder 2/./filename"*

For example, if you want to create a folder on the C drive called config and place it in the Program Files/MyApp folder, use the following command:

*FLfile.createFolder("file:///C\|/Program Files/MyApp/config");*

If you then want to place a file called config.ini in that folder, use the following command:

*FLfile.write("file:///C\|/Program Files/MyApp/config/config.ini", "");*

To create a folder on the Macintosh, you could use the following command:

*FLfile.createFolder("file:///Macintosh/MyApp/config");*

#### Method summary

The following methods can be used with the FLfile object:

| **Method**                             | **Description**                               |
|----------------------------------------|-----------------------------------------------|
| [FLfile.copy()](/FLfile_object/FLfile.md)        | Copies a file.                                |
| [FLfile.createFolder()](/FLfile_object/FLfile1.md) | Creates one or more folders.                  |
| [FLfile.exists()](/FLfile_object/FLfile2.md)       | Determines the existence of a file or folder. |

| **Method**                                       | **Description**                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [FLfile.getAttributes()](/FLfile_object/FLfile3.md)          | Finds out whether a file is writable, read-only, hidden, visible, or a system folder.                             |
| [FLfile.getCreationDate()](/FLfile_object/FLfile4.md)        | Specifies how many seconds have passed between January 1, 1970 and the time the file or folder was created.       |
| [FLfile.getCreationDateObj()](/FLfile_object/FLfile5.md)     | Gets the date a file or folder was created.                                                                       |
| [FLfile.getModificationDate()](/FLfile_object/FLfile6.md)    | Specifies how many seconds have passed between January 1, 1970 and the time the file or folder was last modified. |
| [FLfile.getModificationDateObj()](/FLfile_object/FLfile7.md) | Gets the date a file or folder was last modified.                                                                 |
| [FLfile.getSize()](/FLfile_object/FLfile8.md)                | Gets the size of a file.                                                                                          |
| [FLfile.listFolder()](/FLfile_object/FLfile9.md)             | Lists the contents of a folder.                                                                                   |
| [FLfile.platformPathToURI()](/FLfile_object/FLfile10.md)      | Converts a filename in a platform-specific format to a file:/// URI.                                              |
| [FLfile.read()](/FLfile_object/FLfile11.md)                   | Reads the contents of a file.                                                                                     |
| [FLfile.remove()](/FLfile_object/FLfile12.md)                 | Deletes a file or folder.                                                                                         |
| [FLfile.setAttributes()](/FLfile_object/FLfile13.md)          | Makes a file or folder read-only, writable, hidden, or visible.                                                   |
| [FLfile.uriToPlatformPath()](/FLfile_object/FLfile14.md)      | Converts a filename expressed as a file:/// URI to a platform- specific format.                                   |
| [FLfile.write()](/FLfile_object/FLfile15.md)                  | Creates, writes to, or appends to a file.                                                                         |

<span id="FLfile.copy()" class="anchor"></span>


## folderItem Object



**Inheritance** [Item object](/Item_object/item_summary.md) > folderItem object

#### Availability

Flash MX 2004.

#### Description

The folderItem object is a subclass of the Item object. There are no unique methods or properties for folderItem. See [Item object](/Item_object/item_summary.md).




## fontItem Object


**Inheritance** [Item object](/Item_object/item_summary.md) > fontItem object

#### Availability

Flash MX 2004.

#### Description

The fontItem object is a subclass of the Item object (see [Item object](/Item_object/item_summary.md)).

#### Property summary

In addition to the Item object properties, the following properties are available for the fontItem object:

| **Property**                                  | **Description**                                                                           |
|-----------------------------------------------|-------------------------------------------------------------------------------------------|
| [fontItem.bitmap](/fontItem_object/fontItem.md)           | Specifies whether the Font item is bitmapped.                                             |
| [fontItem.bold](/fontItem_object/fontIte1.md)                | Specifies whether the Font item is bold.                                                  |
| [fontItem.embeddedCharacters](/fontItem_object/fontIte2.md)  | Specifies characters to embed.                                                            |
| [fontItem.embedRanges](/fontItem_object/fontIte3.md)         | Specifies items that can be selected in the Font Embedding dialog.                        |
| [fontItem.embedVariantGlyphs](/fontItem_object/fontIte4.md)  | Specifies whether variant glyphs should be output in the font when publishing a SWF file. |
| [fontItem.font](/fontItem_object/fontIte5.md)                | The name of the device font associated with the Font item.                                |
| [fontItem.isDefineFont4Symbol](/fontItem_object/fontIte6.md) | Specifies the format of the font that is output when publishing a SWF filem.              |
| [fontItem.italic](/fontItem_object/fontIte7.md)              | Specifies whether the Font item is italic.                                                |
| [fontItem.size](/fontItem_object/fontIte8.md)                | The size of the Font item, in points.                                                     |

<span id="fontItem.bitmap" class="anchor"></span>



## Frame Object


#### Availability

Flash MX 2004.

#### Description

The Frame object represents frames in the layer.

#### Method summary

The following methods can be used with the Frame object:

<table><thead><tr class="header"><th><strong>Method</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/Frame_object/frame.md">frame.convertMotionObjectTo2D()</a></td><td>Converts the selected motion object to a 2D motion object.</td></tr><tr class="even"><td><a href="/Frame_object/frame1.md">frame.convertMotionObjectTo3D()</a></td><td>Converts the selected motion object to a 3D motion object.</td></tr><tr class="odd"><td><a href="/Frame_object/frame2.md">frame.convertToFrameByFrameAnimation()</a></td><td>Converts the current frame to Frame-by-Frame Animation.</td></tr><tr class="even"><td><a href="/Frame_object/frame6.md">frame.getCustomEase()</a></td><td><p>Returns an array of JavaScript objects, each of which has an <em>x</emand <em>y</em></p><p>property.</p></td></tr><tr class="odd"><td><a href="/Frame_object/frame7.md">frame.getMotionObjectXML()</a></td><td>Returns the motion XML from the selected motion object.</td></tr><tr class="even"><td><a href="/Frame_object/frame8.md">frame.getSoundEnvelope()</a></td><td>Gets the sound envelope data of any frame.</td></tr><tr class="odd"><td><a href="/Frame_object/frame9.md">frame.getSoundEnvelopeLimits()</a></td><td>Gets the limits (start, end) for a custom Sound envelope that is applied to the frame sound.</td></tr><tr class="even"><td><a href="/Frame_object/frame11.md">frame.hasMotionPath()</a></td><td>Informs you whether or not the currrent selection has a motion tween.</td></tr><tr class="odd"><td><a href="/Frame_object/frame12.md">frame.is3DMotionObject()</a></td><td>Informs you whether or not the currrent selection is a 3D motion object.</td></tr><tr class="even"><td><a href="/Frame_object/frame13.md">frame.isEmpty()</a></td><td>Informs you whether the frame contains any elements.</td></tr><tr class="odd"><td><a href="/Frame_object/frame14.md">frame.isMotionObject()</a></td><td>Informs you whether or not the currrent selection is a motion object.</td></tr><tr class="even"><td><a href="/Frame_object/frame23.md">frame.selectMotionPath()</a></td><td>Selects or deselects the motion path of the current motion object.</td></tr><tr class="odd"><td><a href="/Frame_object/frame24.md">frame.setCustomEase()</a></td><td>Specifies a cubic Bézier curve to be used as a custom ease curve.</td></tr><tr class="even"><td><a href="/Frame_object/frame25.md">frame.setMotionObjectDuration()</a></td><td>Specifies the duration (the tween span length) of the currently selected motion object.</td></tr><tr class="odd"><td><a href="/Frame_object/frame26.md">frame.setMotionObjectXML()</a></td><td>Applies the specified motion XML to the selected motion object.</td></tr><tr class="even"><td><a href="/Frame_object/frame27.md">frame.setSoundEnvelope()</a></td><td>Sets the sound envelope data of a frame.</td></tr><tr class="odd"><td><a href="/Frame_object/frame28.md">frame.setSoundEnvelopeLimits()</a></td><td>Sets the sound envelope limits of any frame with a sound file.</td></tr></tbody></table>

#### Property summary

The following properties can be used with the Frame object:

| **Property**                                   | **Description**                                                                                                                                                                                           |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [frame.actionScript](/Frame_object/frame3.md)            | A string representing ActionScript code.                                                                                                                                                                  |
| [frame.duration](/Frame_object/frame4.md)                | Read-only; an integer that represents the number of frames in a frame sequence.                                                                                                                           |
| [frame.elements](/Frame_object/frame5.md)                | Read-only; an array of Element objects (see [Element object](/Element_object/element_summary.md)).                                                                                                                             |
| [frame.hasCustomEase](/Frame_object/frame10.md)           | A Boolean value that specifies whether the frame gets its ease information from the custom ease curve.                                                                                                    |
| [frame.labelType](/Frame_object/frame15.md)               | A string that specifies the type of Frame name.                                                                                                                                                           |
| [frame.motionTweenOrientToPath](/Frame_object/frame16.md) | A Boolean value that specifies whether or not the tweened element rotates the element as it moves along a path to maintain its angle with respect to each point on the path.                              |
| [frame.motionTweenRotate](/Frame_object/frame17.md)       | A string that specifies how the tweened element rotates.                                                                                                                                                  |
| [frame.motionTweenRotateTimes](/Frame_object/frame18.md)  | An integer that specifies the number of times the tweened element rotates between the starting keyframe and the next keyframe.                                                                            |
| [frame.motionTweenScale](/Frame_object/frame19.md)        | A Boolean value that specifies whether the tweened element scales to the size of the object in the following keyframe, increasing its size with each frame in the tween (true), or doesn’t scale (false). |
| [frame.motionTweenSnap](/Frame_object/frame20.md)         | A Boolean value that specifies whether the tweened element automatically snaps to the nearest point on the motion guide layer associated with this frame’s layer (true) or not (false).                   |
| [frame.motionTweenSync](/Frame_object/frame21.md)         | A Boolean value that if set to true, synchronizes the animation of the tweened object with the main timeline.                                                                                             |
| [frame.name](/Frame_object/frame22.md)                    | A string that specifies the name of the frame.                                                                                                                                                            |
| [frame.shapeTweenBlend](/Frame_object/frame29.md)         | A string that specifies how a shape tween is blended between the shape in the keyframe at the start of the tween and the shape in the following keyframe.                                                 |
| [frame.soundEffect](/Frame_object/frame30.md)             | A string that specifies effects for a sound that is attached directly to a frame ([frame.soundLibraryItem](/Frame_object/frame31.md)).                                                                               |
| [frame.soundLibraryItem](/Frame_object/frame31.md)        | A library item (see [SoundItem object](/SoundItem_object/soundItem_summary.md)) used to create a sound.                                                                                                                            |
| [frame.soundLoop](/Frame_object/frame32.md)               | An integer value that specifies the number of times a sound that is attached directly to a frame ([frame.soundLibraryItem](/Frame_object/frame31.md)) plays.                                                         |
| [frame.soundLoopMode](/Frame_object/frame33.md)           | A string that specifies whether a sound that is attached directly to a frame ([frame.soundLibraryItem](/Frame_object/frame31.md)) should play a specific number of times or loop indefinitely.                       |
| [frame.soundName](/Frame_object/frame34.md)               | A string that specifies the name of a sound that is attached directly to a frame ([frame.soundLibraryItem](/Frame_object/frame31.md)), as stored in the library.                                                     |
| [frame.soundSync](/Frame_object/frame35.md)               | A string that specifies the sync behavior of a sound that is attached directly to a frame ([frame.soundLibraryItem](/Frame_object/frame31.md)).                                                                      |
| [frame.startFrame](/Frame_object/frame36.md)              | Read-only; the index of the first frame in a sequence.                                                                                                                                                    |
| [frame.tweenEasing](/Frame_object/frame37.md)             | An integer that specifies the amount of easing that should be applied to the tweened object.                                                                                                              |
| [frame.tweenInstanceName](/Frame_object/frame38.md)       | Assings an instance name to the specified motion object.                                                                                                                                                  |
| [frame.tweenType](/Frame_object/frame39.md)               | A string that specifies the type of tween.                                                                                                                                                                |
| [frame.useSingleEaseCurve](/Frame_object/frame40.md)      | A Boolean value that specifies whether a single custom ease curve is used for easing information for all properties.                                                                                      |

<span id="frame.convertMotionObjectTo2D()" class="anchor"></span>


## HalfEdge Object


#### Availability

Flash MX 2004.

#### Description

The HalfEdge object is the directed side of the edge of a [Shape object](/Shape_object/shape_summary.md). An edge has two half edges. You can transverse the contours of a shape by "walking around" these half edges. For example, starting from a half edge, you can trace all the half edges around a contour of a shape, and return to the original half edge.
Half edges are ordered. One half edge represents one side of the edge; the other half edge represents the other side.

#### Method summary

The following methods are available for the HalfEdge object:

| **Method**                                      | **Description**                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------|
| [halfEdge.getEdge()](/HalfEdge_object/halfEdge.md)       | Gets the [Edge object](/Edge_object/edge_summary.md) for the HalfEdge object.               |
| [halfEdge.getNext()](/HalfEdge_object/halfEdg1.md)             | Gets the next half edge on the current contour.                              |
| [halfEdge.getOppositeHalfEdge()](/HalfEdge_object/halfEdg2.md) | Gets the HalfEdge object on the other side of the edge.                      |
| [halfEdge.getPrev()](/HalfEdge_object/halfEdg3.md)             | Gets the preceding HalfEdge object on the current contour.                   |
| [halfEdge.getVertex()](/HalfEdge_object/halfEdg4.md)           | Gets the [Vertex object](/Vertex_object/vertex_summary.md) at the head of the HalfEdge object. |

#### Property summary

The following properties are available for the HalfEdge object:

| **Property**                 | **Description**                                                 |
|------------------------------|-----------------------------------------------------------------|
| [halfEdge.id](/HalfEdge_object/halfEdg5.md) | Read-only; a unique integer identifier for the HalfEdge object. |

<span id="halfEdge.getEdge()" class="anchor"></span>




## Instance Object


**Inheritance** [Element object](/Element_object/element_summary.md) > Instance object

#### Availability

Flash MX 2004.

#### Description

Instance is a subclass of the [Element object](/Element_object/element_summary.md).

#### Property summary

In addition to all of the Element object properties, Instance has the following properties:

| **Property**                                    | **Description**                                           |
|-------------------------------------------------|-----------------------------------------------------------|
| [instance.instanceType](/Instance_object/instance.md) | Read-only; a string that represents the type of instance. |
| [instance.libraryItem](/Instance_object/instanc1.md)           | Library item used to instantiate this instance.           |

<span id="instance.instanceType" class="anchor"></span>



## Item Object


#### Availability

Flash MX 2004.

#### Description

The Item object is an abstract base class. Anything in the library derives from Item. See also [library object](/library_object/library_summary.md).

#### Method summary

The following methods are available for the Item object:

| **Method**                             | **Description**                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [item.addData()](/Item_object/item.md)      | Adds specified data to a library item.                                                                                         |
| [item.getData()](/Item_object/item1.md)        | Retrieves the value of the specified data.                                                                                     |
| [item.getPublishData()](/Item_object/item2.md) | Indicates whether publishing of the specified persistent data is enabled for the specified format on a specified library item. |
| [item.hasData()](/Item_object/item3.md)        | Determines whether the library item has the named data.                                                                        |
| [item.removeData()](/Item_object/item14.md)     | Removes persistent data from the library item.                                                                                 |
| [item.setPublishData()](/Item_object/item15.md) | Enables publishing of persistent data for a library item.                                                                      |

#### Property summary

The following properties are available for the Item object:

| **Property**                                    | **Description**                                                                                                 |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [item.itemType](/Item_object/item4.md)                  | Read-only; a string that specifies the type of element.                                                         |
| [item.linkageBaseClass](/Item_object/item5.md)          | A string that specifies the ActionScript 3.0 class that will be associated with the symbol.                     |
| [item.linkageClassName](/Item_object/item6.md)          | A string that specifies the ActionScript 2.0 class that will be associated with the symbol.                     |
| [item.linkageExportForAS](/Item_object/item7.md)        | A Boolean value. If true, the item is exported for ActionScript.                                                |
| [item.linkageExportForRS](/Item_object/item8.md)        | A Boolean value. If true, the item is exported for run-time sharing.                                            |
| [item.linkageExportInFirstFrame](/Item_object/item9.md) | A Boolean value. If true, the item is exported in the first frame.                                              |
| [item.linkageIdentifier](/Item_object/item10.md)         | A string that specifies the name Animate will use to identify the asset when linking to the destination SWF file. |
| [item.linkageImportForRS](/Item_object/item11.md)        | A Boolean value. If true, the item is imported for run-time sharing.                                            |
| [item.linkageURL](/Item_object/item12.md)                | A string that specifies the URL where the SWF file containing the shared asset is located.                      |
| [item.name](/Item_object/item13.md)                      | A string that specifies the name of the library item, which includes the folder structure.                      |

<span id="item.addData()" class="anchor"></span>



## Layer Object


#### Availability

Flash MX 2004.

#### Description

The Layer object represents a layer in the timeline. The [timeline.layers](/Timeline_object/timeli31.md) property contains an array of Layer objects, which can be accessed by fl.getDocumentDOM().getTimeline().layers.

#### Method summary

The following methods are available for the Item object:

| **Method**                             | **Description**                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [layer.getBlendModeAtFrame()](/Layer_object/layer13.md)      | A string value that specifies the blend mode at frame.                                                                                         |
| [layer.getColorTransformAtFrame()](/Layer_object/layer14.md)        | Based on the mode, the paramters will be updated here. For example, if tint is present, the value corresponding to tint only will be present along with the color matrix values..                                                                                     |
| [layer.getFiltersAtFrame()](/Layer_object/layer15.md)      | An array that contains a list of filters applied to the frame at frameIndex.                                                                                         |
| [layer.getZDepthAtFrame() ](/Layer_object/layer11.md)      | An integer value that specifies the ZDepth valur at the frame.                                                                                         |
| [layer.setBlendModeAtFrame()](/Layer_object/layer16.md)      |FrameNumber :frame index,  ZVal:int.                                                                                         |
| [layer.setColorTransformAtFrame()](/Layer_object/layer17.md)      | frameIndex – int, cxFormObject - The cxform to be set   .                                                                                         |
| [layer. setFiltersAtFrame()](/Layer_object/layer18.md)      | frameIndex – int, filterArray - The array of filters to be set.                                                                                         |
| [layer.setZDepthAtFrame() ](/Layer_object/layer12.md)        | Enables to set ZDepth value at the frame.                                                                                     |

#### Property summary

The following properties are available for the Layer object:

| **Property**                                                         | **Description**                                                                                                                 |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [layer.animationType](/Layer_object/layer.md)| The layer type: "none", "motion object", or "IK pose".                                                                          |
| [layer.color](/Layer_object/layer1.md)                                         | A string, hexadecimal value, or integer that specifies the color assigned to outline the layer.                                 |
| [layer.frameCount](/Layer_object/layer2.md)                                    | Read-only; an integer that specifies the number of frames in the layer.                                                         |
| [layer.frames](/Layer_object/layer3.md)                                        | Read-only; an array of Frame objects.                                                                                           |
| [layer.height](/Layer_object/layer4.md)                                        | An integer that specifies the percentage layer height; equivalent to the Layer height value in the Layer Properties dialog box. |
| [layer.layerType](/Layer_object/layer5.md)                                     | A string that specifies the current use of the layer; equivalent to the Type setting in the Layer Properties dialog box.        |
| [layer.locked](/Layer_object/layer6.md)                                        | A Boolean value that specifies the locked status of the layer.                                                                  |
| [layer.name](/Layer_object/layer7.md)                                          | A string that specifies the name of the layer.                                                                                  |
| [layer.outline](/Layer_object/layer8.md)                                       | A Boolean value that specifies the status of outlines for all objects in the layer.                                             |
| [layer.parentLayer](/Layer_object/layer9.md)                                   | A Layer object that represents the layer’s containing folder, guiding, or masking layer.                                        |
| [layer.visible](/Layer_object/layer10.md)                                       | A Boolean value that specifies whether the layer’s objects on the Stage are shown or hidden.                                    |

<span id="layer.animationType" class="anchor"></span>


    
## LayerParenting Object


#### Availability

Adobe Animate 2020.

#### Method summary

You can use the following methods with the layer object:

| **Method**                    | **Usage**                                     |
|-------------------------------|-----------------------------------------------|
| [layer.getRigMatrixAtFrame()](/Layer_Parenting_Object/layerParenting3.md) | layer.getRigMatrixAtFrame(frameIndex)           |
| [layer.getRigParentAtFrame()](/Layer_Parenting_Object/layerParenting1.md) | layer.getRigParentAtFrame(frameIndex)       |
| [layer.setRigParentAtFrame()](/Layer_Parenting_Object/layerParenting2.md) | layer.setRigParentAtFrame(frameIndex,layer)   |



## library Object


#### Availability

Flash MX 2004.

#### Description

The library object represents the Library panel. It is a property of the Document object (see [document.library](/Document_object/docume98.md)) and can be accessed by *fl.getDocumentDOM().library*.

The library object contains an array of items of different types, including symbols, bitmaps, sounds, and video.

#### Method summary

The following methods are available for the library object:

| **Method**                                                  | **Description**                                                                                                                                                  |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [library.addItemToDocument()](/library_object/library.md) | Adds the current or specified item to the Stage at the specified position.                                                                                       |
| [library.addNewItem()](/library_object/library1.md)                       | Creates a new item of the specified type in the Library panel and sets the new item to the currently selected item.                                              |
| [library.deleteItem()](/library_object/library2.md)                       | Deletes the current items or a specified item from the Library panel.                                                                                            |
| [library.duplicateItem()](/library_object/library3.md)                    | Makes a copy of the currently selected or specified item.                                                                                                        |
| [library.editItem()](/library_object/library4.md)                         | Opens the currently selected or specified item in Edit mode.                                                                                                     |
| [library.findItemIndex()](/library_object/library5.md)                    | Returns the library item’s index value (zero-based).                                                                                                             |
| [library.getItemProperty()](/library_object/library6.md)                  | Gets the property for the selected item.                                                                                                                         |
| [library.getItemType()](/library_object/library7.md)                      | Gets the type of object currently selected or specified by a library path.                                                                                       |
| [library.getSelectedItems()](/library_object/library8.md)                 | Gets the array of all currently selected items in the library.                                                                                                   |
| [library.itemExists()](/library_object/library9.md)                       | Checks to see if a specified item exists in the library.                                                                                                         |
| [library.moveToFolder()](/library_object/librar11.md)                     | Moves the currently selected or specified library item to a specified folder.                                                                                    |
| [library.newFolder()](/library_object/librar12.md)                        | Creates a new folder with the specified name, or a default name (*"untitled folder \#"*) if no folderName parameter is provided, in the currently selected folder. |
| [library.renameItem()](/library_object/librar13.md)                       | Renames the currently selected library item in the Library panel.                                                                                                |
| [library.selectAll()](/library_object/librar14.md)                        | Selects or deselects all items in the library.                                                                                                                   |
| [library.selectItem()](/library_object/librar15.md)                       | Selects a specified library item.                                                                                                                                |
| [library.selectNone()](/library_object/librar16.md)                       | Deselects all the library items.                                                                                                                                 |
| [library.setItemProperty()](/library_object/librar17.md)                  | Sets the property for all selected library items (ignoring folders).                                                                                             |
| [library.updateItem()](/library_object/librar19.md)                       | Updates the specified item.                                                                                                                                      |

#### Property summary for the library object

The following property is available for the library object:

| **Property**                         | **Description**                                              |
|--------------------------------------|--------------------------------------------------------------|
| [library.items](/library_object/librar10.md)       | An array of Item objects in the library                      |
| [library.unusedItems](/library_object/librar18.md) | An array of library Items that are not used in the document. |

<span id="library.addItemToDocument()" class="anchor"></span>



## Math Object


#### Availability

Flash MX 2004.

#### Description

The Math object is available as a read-only property of the flash object; see [fl.Math](/flash_object_(fl)/fl41.md). This object provides methods that perform common mathematical operations.

#### Method summary

The following methods are available for the Math object:

| **Method**                                  | **Description**                                         |
|---------------------------------------------|---------------------------------------------------------|
| [Math.concatMatrix()](/Math_object/Math.md) | Performs a matrix concatenation and returns the result. |
| [Math.invertMatrix()](/Math_object/Math1.md)        | Returns the inverse of the specified matrix.            |
| [Math.pointDistance()](/Math_object/Math2.md)       | Computes the distance between two points.               |
| [Math.transformPoint()](/Math_object/Math3.md)      | Applies a matrix to a point.                            |

<span id="Math.concatMatrix()" class="anchor"></span>



## Matrix Object


#### Availability

Flash MX 2004.

#### Description

The Matrix object represents a transformation matrix.

#### Property summary

The following properties are available for the Matrix object:

| **Property**               | **Description**                                                                                                        |
|----------------------------|------------------------------------------------------------------------------------------------------------------------|
| [matrix.a](/Matrix_object/matrix.md)      | A floating-point value that specifies the (0,0) element in the transformation matrix.                                  |
| [matrix.b](/Matrix_object/matrix1.md)  | A floating-point value that specifies the (0,1) element in the matrix.                                                 |
| [matrix.c](/Matrix_object/matrix2.md)  | A floating-point value that specifies the (1,0) element in the matrix.                                                 |
| [matrix.d](/Matrix_object/matrix3.md)  | A floating-point value that specifies the (1,1) element in the matrix.                                                 |
| [matrix.tx](/Matrix_object/matrix4.md) | A floating-point value that specifies the *x*-axis location of a symbol’s registration point or the center of a shape. |
| [matrix.ty](/Matrix_object/matrix5.md) | A floating-point value that specifies the *y*-axis location of a symbol’s registration point or the center of a shape. |

<span id="matrix.a" class="anchor"></span>



## outputPanel Object


#### Availability

Flash MX 2004.

#### Description

This object represents the Output panel, which displays troubleshooting information such as syntax errors. To access this object, use fl.outputPanel (or flash.outputPanel). See [fl.outputPanel](/flash_object_(fl)/fl47.md).

#### Method summary

The outputPanel object uses the following methods:

| **Method**                                  | **Description**                                                            |
|---------------------------------------------|----------------------------------------------------------------------------|
| [outputPanel.clear()](/outputPanel_object/outputPanel.md) | Clears the contents of the Output panel.                                   |
| [outputPanel.save()](/outputPanel_object/outputPane1.md)         | Saves the contents of the Output panel to a local text file.               |
| [outputPanel.trace()](/outputPanel_object/outputPane2.md)        | Adds a line to the contents of the Output panel, terminated by a new line. |

<span id="outputPanel.clear()" class="anchor"></span>



## Oval Object


**Inheritance** [Element object](/Element_object/element_summary.md) >[Shape object](/Shape_object/shape_summary.md) Oval object

#### Availability

Flash CS3 Professional.

#### Description

The Oval object is a shape that is drawn using the Oval Primitive tool. To determine if an item is an Oval object, use
[shape.isOvalObject](/Shape_object/shape9.md).

#### Property summary

In addition to the [Shape object](/Shape_object/shape_summary.md) properties, you can use the following properties with the Oval object. To set the properties of an Oval object, use [document.setOvalObjectProperty()](/Document_object/docum590.md).

| **Property**                                  | **Description**                                                                                                   |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [OvalObject.closePath](/Oval_object/OvalObject.md) | Read-only; a Boolean value that specifies whether the Close Path check box in the Property inspector is selected. |
| [OvalObject.endAngle](/Oval_object/OvalObjec1.md)          | Read-only; a float value that specifies the end angle of the Oval object.                                         |
| [OvalObject.innerRadius](/Oval_object/OvalObjec2.md)       | Read-only; a float value that specifies the inner radius of the Oval object as a percentage.                      |
| [OvalObject.startAngle](/Oval_object/OvalObjec3.md)        | Read-only; a float value that specifies the start angle of the Oval object.                                       |

<span id="OvalObject.closePath" class="anchor"></span>



## Parameter object


#### Availability

Flash MX 2004.

#### Description

The Parameter object type is accessed from the [componentInstance.parameters](/ComponentInstance_object/componentInstance.md) array (which corresponds to the component Property inspector in the authoring tool).

#### Method summary

The following methods are available for the Parameter object:

| **Method**                              | **Description**                                                                    |
|-----------------------------------------|------------------------------------------------------------------------------------|
| [parameter.insertItem()](/Parameter_object/paramete1.md) | Inserts an item into an object or array.                                           |
| [parameter.removeItem()](/Parameter_object/paramete4.md) | Removes an element of the object or array type of a screen or component parameter. |

#### Property summary

The following properties are available for the Parameter object:

<table><thead><tr class="header"><th><strong>Property</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/Parameter_object/parameter.md">parameter.category</a></td><td><p>A string that specifies the category property for the screen parameter or</p><p>componentInstance parameter.</p></td></tr><tr class="even"><td><a href="/Parameter_object/paramete2.md">parameter.listIndex</a></td><td>An integer that specifies the value of the selected list item.</td></tr><tr class="odd"><td><a href="/Parameter_object/paramete3.md">parameter.name</a></td><td>Read-only; a string that specifies the name of the parameter.</td></tr><tr class="even"><td><a href="/Parameter_object/paramete5.md">parameter.value</a></td><td>Corresponds to the Value field in the Parameters tab of the Component inspector, the Parameters tab of the Property inspector, or the screen Property inspector.</td></tr><tr class="odd"><td><a href="/Parameter_object/paramete6.md">parameter.valueType</a></td><td>Read-only; a string that indicates the type of the screen or component parameter.</td></tr><tr class="even"><td><a href="/Parameter_object/paramete7.md">parameter.verbose</a></td><td>Specifies where the parameter is displayed.</td></tr></tbody></table>

<span id="parameter.category" class="anchor"></span>


 
## Path object

#### Availability

Flash MX 2004.

#### Description

The Path object defines a sequence of line segments (straight, curved, or both), which you typically use when creating extensible tools. The following example shows an instance of a Path object being returned from the flash object:

path = fl.drawingLayer.newPath();

See also the [drawingLayer object](/drawingLayer_object/drawingLayersummary.md).

#### Method summary

The following methods are available for the Path object:

| **Method**                                    | **Description**                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [path.addCubicCurve()](/Path_object/path.md) | Appends a cubic Bézier curve segment to the path.                                                                         |
| [path.addCurve()](/Path_object/path1.md)              | Appends a quadratic Bézier segment to the path.                                                                           |
| [path.addPoint()](/Path_object/path2.md)              | Adds a point to the path.                                                                                                 |
| [path.clear()](/Path_object/path3.md)                 | Removes all points from the path.                                                                                         |
| [path.close()](/Path_object/path4.md)                 | Appends a point at the location of the first point of the path and extends the path to that point, which closes the path. |
| [path.makeShape()](/Path_object/path5.md)             | Creates a shape on the Stage by using the current stroke and fill settings.                                               |
| [path.newContour()](/Path_object/path6.md)            | Starts a new contour in the path.                                                                                         |

#### Property summary

The following properties are available for the Path object:

| **Property**               | **Description**                                                      |
|----------------------------|----------------------------------------------------------------------|
| [path.nPts](/Path_object/path7.md) | Read-only; an integer representing the number of points in the path. |

<span id="path.addCubicCurve()" class="anchor"></span>



## presetItem object


#### Availability

Flash CS4 Professional.

#### Description

The presetItem object represents an item (preset or folder) in the Motion Presets panel (Window > Motion Presets). The array of presetItem objects is a property of the presetPanel object ([presetPanel.items](/presetPanel_object/presetPane9.md)).

All properties of the presetItem object are read only. To perform tasks such as deleting, renaming, or moving items, use the methods of the [presetPanel object](/presetPanel_object/presetPanel_summary.md).

#### Property summary

You can use the following properties with the presetItem object:

| **Property**                                  | **Description**                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [presetItem.isDefault](/presetItem_object/presetItem.md) | Specifies whether the item is installed along with Flash or is a custom item that you or someone else has created. |
| [presetItem.isFolder](/presetItem_object/presetIte1.md)          | Specifies whether the item in the Motion Presets panel is a folder or a preset.                                    |
| [presetItem.level](/presetItem_object/presetIte2.md)             | The level of the item in the folder structure of the Motion Presets panel.                                         |
| [presetItem.name](/presetItem_object/presetIte3.md)              | The name of the preset or folder, without path information.                                                        |
| [presetItem.open](/presetItem_object/presetIte4.md)              | Specifies whether a folder in the Motion Presets panel is currently expanded.                                      |
| [presetItem.path](/presetItem_object/presetIte5.md)              | The path to the item in the Motion Presets panel folder tree, and the item name.                                   |

<span id="presetItem.isDefault" class="anchor"></span>



## presetPanel object


#### Availability

Flash CS4 Professional.

#### Description

The presetPanel object represents the Motion Presets panel (Window > Motion Presets). It is a property of the flash object ([fl.presetPanel](/flash_object_(fl)/fl49.md)).

#### Method summary

You can use the following methods with the presetPanel object:

| **Method**                                            | **Description**                                                                                                   |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [presetPanel.addNewItem()](/presetPanel_object/presetPanel.md) | If a single motion tween is currently selected on the Stage, adds that motion to the Motion Presets panel.        |
| [presetPanel.applyPreset()](/presetPanel_object/presetPane1.md)            | Applies the specified or currently selected preset to the currently selected item on the Stage.                   |
| [presetPanel.deleteFolder()](/presetPanel_object/presetPane2.md)           | Deletes the specified folder and any of its subfolders from the folder tree of the Motion Presets panel.          |
| [presetPanel.deleteItem()](/presetPanel_object/presetPane3.md)             | Deletes the specified preset from the Motion Presets panel.                                                       |
| [presetPanel.expandFolder()](/presetPanel_object/presetPane4.md)           | Expands or collapses the currently selected folder or folders in the Motion Presets panel.                        |
| [presetPanel.exportItem()](/presetPanel_object/presetPane5.md)             | Exports the currently selected or the specified preset to an XML file.                                            |
| [presetPanel.findItemIndex()](/presetPanel_object/presetPane6.md)          | Returns an integer that represents the index location of an item in the Motion Presets panel.                     |
| [presetPanel.getSelectedItems()](/presetPanel_object/presetPane7.md)       | Returns an array of presetItem objects corresponding to the currently selected items in the Motion Presets panel. |
| [presetPanel.importItem()](/presetPanel_object/presetPane8.md)             | Adds a preset to the Motion Presets panel from a specified XML file.                                              |
| [presetPanel.moveToFolder()](/presetPanel_object/presetPan10.md)           | Moves the specified item to the specified folder.                                                                 |
| [presetPanel.newFolder()](/presetPanel_object/presetPan11.md)              | Creates a folder in the folder tree of the Motion Presets panel.                                                  |
| [presetPanel.renameItem()](/presetPanel_object/presetPan12.md)             | Renames the currently selected preset or folder to a specified name.                                              |
| [presetPanel.selectItem()](/presetPanel_object/presetPan13.md)             | Selects or deselects an item in the Motion Presets panel.                                                         |

#### Property summary

You can use the following property with the presetPanel object:

| **Property**                       | **Description**                                             |
|------------------------------------|-------------------------------------------------------------|
| [presetPanel.items](/presetPanel_object/presetPane9.md) | An array of presetItem objects in the Motion Presets panel. |

<span id="presetPanel.addNewItem()" class="anchor"></span>




## Rectangle object


**Inheritance** [Element object](/Element_object/element_summary.md) > [Shape object](/Shape_object/shape_summary.md) > Rectangle object

#### Availability

Flash CS3 Professional.

#### Description

The Rectangle object is a shape that is drawn using the Rectangle Primitive tool. To determine if an item is a Rectangle object, use [shape.isRectangleObject](/Shape_object/shape10.md).

#### Property summary

In addition to the [Shape object](/Shape_object/shape_summary.md) properties, you can use the following properties with the Rectangle object. To set the properties of a Rectangle object, use [document.setRectangleObjectProperty()](/Document_object/docu9643.md).

| **Property**                                                          | **Description**                                                                                                                                            |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RectangleObject.bottomLeftRadius](/Rectangle_object/RectangleObject.md) | Read-only; a float value that sets the radius of the bottom-left corner of the Rectangle object.                                                           |
| [RectangleObject.bottomRightRadius](/Rectangle_object/RectangleObjec1.md)                    | Read-only; a float value that sets the radius of the bottom-right corner of the Rectangle object.                                                          |
| [RectangleObject.lockFlag](/Rectangle_object/RectangleObjec2.md)                             | Read-only; a Boolean value that determines whether different corners of the rectangle can have different radius values.                                    |
| [RectangleObject.topLeftRadius](/Rectangle_object/RectangleObjec3.md)                        | Read-only; a float value that sets the radius of all corners of the rectangle or that sets only the radius of the top-left corner of the Rectangle object. |
| [RectangleObject.topRightRadius](/Rectangle_object/RectangleObjec4.md)                       | Read-only; a float value that sets the radius of the top-right corner of the Rectangle object.                                                             |

<span id="RectangleObject.bottomLeftRadius" class="anchor"></span>




## Shape object


**Inheritance** [Element object](/Element_object/element_summary.md) > Shape object

#### Availability

Flash MX 2004.

#### Description

The Shape object is a subclass of the Element object. The Shape object provides more precise control than the drawing APIs when manipulating or creating geometry on the Stage. This control is necessary so that scripts can create useful effects and other drawing commands (see [Element object](/Element_object/element_summary.md)).
All Shape methods and properties that change a shape or any of its subordinate parts must be placed between
[shape.beginEdit()](/Shape_object/shape.md) and [shape.endEdit()](/Shape_object/shape4.md) calls to function correctly.

#### Method summary

In addition to the Element object methods, you can use the following methods with the Shape object:

| **Method**                                     | **Description**                                       |
|------------------------------------------------|-------------------------------------------------------|
| [shape.getCubicSegmentPoints()](/Shape_object/shape5.md) | Returns an array of points that define a cubic curve. |
| [shape.beginEdit()](/Shape_object/shape.md)        | Defines the start of an edit session.                 |
| [shape.deleteEdge()](/Shape_object/shape2.md)            | Deletes the specified edge.                           |
| [shape.endEdit()](/Shape_object/shape4.md)               | Defines the end of an edit session for the shape.     |

#### Property summary

In addition to the Element object properties, the following properties are available for the Shape object:

| **Property**                             | **Description**                                                                                       |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [shape.contours](/Shape_object/shape1.md)          | Read-only; an array of Contour objects for the shape (see [Contour object](/Contour_object/contour_summary.md)).           |
| [shape.edges](/Shape_object/shape3.md)             | Read-only; an array of Edge objects (see [Edge object](/Edge_object/edge_summary.md)).                               |
| [shape.isDrawingObject](/Shape_object/shape6.md)   | Read-only; if true, the shape is a drawing object.                                                    |
| [shape.isFloating](/Shape_object/shape7.md)        | Read-only; if true, the shape is floating above the parent frame's (or group's) shape.                |
| [shape.isGroup](/Shape_object/shape8.md)           | Read-only; if true, the shape is a group.                                                             |
| [shape.isOvalObject](/Shape_object/shape9.md)      | Read-only; if true, the shape is a primitive Oval object (was created using the Oval tool).           |
| [shape.isRectangleObject](/Shape_object/shape10.md) | Read-only; if true, the shape is a primitive Rectangle object (was created using the Rectangle tool). |
| [shape.members](/Shape_object/shape11.md)           | An array of objects in the currently selected group.                                                  |
| [shape.numCubicSegments](/Shape_object/shape12.md)  | Read-only; the number of cubic segments in the shape.                                                 |
| [shape.vertices](/Shape_object/shape13.md)          | Read-only; an array of Vertex objects (see [Vertex object](/Vertex_object/vertex_summary.md)).                          |

<span id="shape.beginEdit()" class="anchor"></span>



## SoundItem object


**Inheritance** [Item object](/Item_object/item_summary.md) > SoundItem object

#### Availability

Flash MX 2004.

#### Description

The SoundItem object is a subclass of the Item object. It represents a library item used to create a sound. See also [frame.soundLibraryItem](/Frame_object/frame31.md) and [Item object](/Item_object/item_summary.md).

#### Method summary

In addition to the Item object methods, the SoundItem object has the following method:

| **Method**                                | **Description**                                                           |
|-------------------------------------------|---------------------------------------------------------------------------|
| [soundItem.exportToFile()](/SoundItem_object/soundIte4.md) | Exports the specified item to an MP3 or WAV file (Macintosh and Windows). |

#### Property summary

In addition to the Item object properties, the following properties are available for the SoundItem object:

| **Property**                                       | **Description**                                                                                                                                                                                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [soundItem.bitRate](/SoundItem_object/soundItem.md)            | A string that specifies the bit rate of a sound in the library. Available only for the MP3 compression type.                                                                                                                                    |
| [soundItem.bits](/SoundItem_object/soundIte1.md)                    | A string that specifies the bits value for a sound in the library that has ADPCM compression.                                                                                                                                                   |
| [soundItem.compressionType](/SoundItem_object/soundIte2.md)         | A string that specifies the compression type for a sound in the library.                                                                                                                                                                        |
| [soundItem.convertStereoToMono](/SoundItem_object/soundIte3.md)     | A Boolean value available only for MP3 and Raw compression types.                                                                                                                                                                               |
| [soundItem.fileLastModifiedDate](/SoundItem_object/soundIte5.md)    | Read-only; a string containing a hexadecimal number that represents the number of seconds that have elapsed between January 1, 1970, and the modification date of the original file (on disk) at the time the file was imported to the library. |
| [soundItem.lastModifiedDate](/SoundItem_object/soundIte6.md)        | Read-only; the modification date of the sound item in the Library.                                                                                                                                                                              |
| [soundItem.originalCompressionType](/SoundItem_object/soundIte7.md) | Read-only; a string that specifies whether the specified item was imported as an MP3 file.                                                                                                                                                      |
| [soundItem.quality](/SoundItem_object/soundIte8.md)                 | A string that specifies the playback quality of a sound in the library. Available only for the MP3 compression type.                                                                                                                            |
| [soundItem.sampleRate](/SoundItem_object/soundIte9.md)              | A string that specifies the sample rate for the audio clip.                                                                                                                                                                                     |
| [soundItem.sourceFileExists](/SoundItem_object/soundIt10.md)        | Read-only; a Boolean value that specifies whether the file that was imported to the Library still exists in the location from where it was imported.                                                                                            |

| **Property**                                     | **Description**                                                                                                                                                              |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [soundItem.sourceFileIsCurrent](/SoundItem_object/soundIt11.md)   | Read-only; a Boolean value that specifies whether the file modification date of the Library item is the same as the modification date on disk of the file that was imported. |
| [soundItem.sourceFilePath](/SoundItem_object/soundIt12.md)        | Read-only; a string, expressed as a file:/// URI, that represents the path and name of the file that was imported into the Library.                                          |
| [soundItem.useImportedMP3Quality](/SoundItem_object/soundIt13.md) | A Boolean value; if true, all other properties are ignored, and the imported MP3 quality is used.                                                                            |

<span id="soundItem.bitRate" class="anchor"></span>



## SpriteSheetExporter object


**Inheritance** [Item object](/Item_object/item_summary.md) >SpriteSheetExporter object

#### Availability

Flash Pro CS6.

#### Description

The SpriteSheetExporter object is a subclass of the [Item object](/Item_object/item_summary.md).

#### Method summary

In addition to the Item object methods, you can use the following methods with the SpriteSheetExporter object:

| **Method**                                                          | **Description**                                                   |
|---------------------------------------------------------------------|-------------------------------------------------------------------|
| [SpriteSheetExporter.addBitmap()](/SpriteSheetExporter_object/SpriteSheetExporter.md) | Adds a bitmap or bitmapItem to the sprite sheet.                  |
| [SpriteSheetExporter.addSymbol()](/SpriteSheetExporter_object/SpriteSheetExporte1.md)                    | Adds a symbol to be used to generate the sprite sheet.            |
| [SpriteSheetExporter.beginExport()](/SpriteSheetExporter_object/SpriteSheetExporte7.md)                  | Initializes the SpriteSheetExporter to create a new sprite sheet. |
| [SpriteSheetExporter.changeSymbol()](/SpriteSheetExporter_object/SpriteSheetExport14.md)                 | Changes which symbol frames will be added to the sprite sheet.    |
| [SpriteSheetExporter.exportSpriteSheet()](/SpriteSheetExporter_object/SpriteSheetExport15.md)            | Export the sprite sheet into a an image file.                     |
| [SpriteSheetExporter.removeBitmap()](/SpriteSheetExporter_object/SpriteSheetExport22.md)                 | Remove a bitmap object from the sprite sheet.                     |
| [SpriteSheetExporter.removeSymbol()](/SpriteSheetExporter_object/SpriteSheetExport23.md)                 | Remove a symbol from the sprite sheet.                            |

#### Property summary

In addition to the Item object properties, the following properties are available for the SpriteSheetExporter object:

| **Property**                                       | **Description**                                                                                                          |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [SpriteSheetExporter.algorithm](/SpriteSheetExporter_object/SpriteSheetExporte2.md)     | Sets the encoding algorithm for the sprite sheet.                                                                        |
| [SpriteSheetExporter.allowRotate](/SpriteSheetExporter_object/SpriteSheetExporte3.md)   | Allows sprites to be rotated when added to the sprite sheet.                                                             |
| [SpriteSheetExporter.allowTrimming](/SpriteSheetExporter_object/SpriteSheetExporte4.md) | Allows trimming of whitespace around sprites.                                                                            |
| [SpriteSheetExporter.app](/SpriteSheetExporter_object/SpriteSheetExporte5.md)           | A string indicating the name of the application generating the sprite sheet.                                             |
| [SpriteSheetExporter.autoSize](/SpriteSheetExporter_object/SpriteSheetExporte6.md)      | Automatically size the sprite sheet to fit all sprites.                                                                  |
| [SpriteSheetExporter.borderPadding](/SpriteSheetExporter_object/SpriteSheetExporte8.md) | The amount of padding around the sprite sheet borders, in pixels.                                                        |
| [SpriteSheetExporter.canBorderPad](/SpriteSheetExporter_object/SpriteSheetExporte9.md)  | A Boolean value indicating whether border padding is supported by the framework specified by the layoutFormat property.  |
| [SpriteSheetExporter.canRotate](/SpriteSheetExporter_object/SpriteSheetExport10.md)     | A Boolean value indicating whether sprite rotation is supported by the framework specified by the layoutFormat property. |
| [SpriteSheetExporter.canShapePad](/SpriteSheetExporter_object/SpriteSheetExport12.md)   | A Boolean value indicating whether shape padding is supported by the framework specified by the layoutFormat property.   |

| **Property**                                                                       | **Description**                                                                                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [SpriteSheetExporter.canStackDuplicateFrames](/SpriteSheetExporter_object/SpriteSheetExport13.md)     | A Boolean value indicating whether sprite stacking is supported by the framework specified by the layoutFormat property. |
| [SpriteSheetExporter.canTrim](/SpriteSheetExporter_object/SpriteSheetExport11.md)                                       | A Boolean value indicating whether shape trimming is supported by the framework specified by the layoutFormat property.  |
| [SpriteSheetExporter.format](/SpriteSheetExporter_object/SpriteSheetExport16.md)                                        | The format of the sprite sheet image file.                                                                               |
| [SpriteSheetExporter.image](/SpriteSheetExporter_object/SpriteSheetExport17.md)                                         | The name of the image file of the sprite sheet.                                                                          |
| [SpriteSheetExporter.layoutFormat](/SpriteSheetExporter_object/SpriteSheetExport18.md)                                  | The format of the sprite sheet metadata.                                                                                 |
| [SpriteSheetExporter.maxSheetHeight](/SpriteSheetExporter_object/SpriteSheetExport19.md) | Controls the maximum height of the generated sprite sheet when autoSize = true, clipped to a maximum value of 8192.      |
| [SpriteSheetExporter.maxSheetWidth](/SpriteSheetExporter_object/SpriteSheetExport20.md)  | Controls the maximum width of the generated sprite sheet when autoSize = true, clipped to a maximum value of 8192.       |
| [SpriteSheetExporter.overflowed](/SpriteSheetExporter_object/SpriteSheetExport21.md)                                    | A Boolean value indicating whether all the specified frames can fit in the specified sprite sheet size.                  |
| [SpriteSheetExporter.shapePadding](/SpriteSheetExporter_object/SpriteSheetExport24.md)                                  | The amount of padding around each sprite, in pixels.                                                                     |
| [SpriteSheetExporter.sheetHeight](/SpriteSheetExporter_object/SpriteSheetExport25.md)                                   | The height of the sprite sheet, in pixels.                                                                               |
| [SpriteSheetExporter.sheetWidth](/SpriteSheetExporter_object/SpriteSheetExport26.md)                                    | The width of the sprite sheet, in pixels.                                                                                |
| [SpriteSheetExporter.stackDuplicate](/SpriteSheetExporter_object/SpriteSheetExport27.md)        | A Boolean value indicating whether to stack identical symbol frames in the sprite sheet.                                 |
| [SpriteSheetExporter.version](/SpriteSheetExporter_object/SpriteSheetExport28.md)                                       | The version number of the application creating the sprite sheet.                                                         |

<span id="SpriteSheetExporter.addBitmap()" class="anchor"></span>




## Stroke object


#### Availability

Flash MX 2004.

#### Description

The Stroke object contains all the settings for a stroke, including the custom settings. This object represents the information contained in the Property inspector. Using the Stroke object together with the [document.setCustomStroke()](/Document_object/docum480.md) method, you can change the stroke settings for the Tools panel, the Property inspector, and the current selection. You can also get the stroke settings of the Tools panel and Property inspector, or of the current selection, by using the [document.getCustomStroke()](/Document_object/docume75.md) method.
This object always has the following four properties: style, thickness, color, and breakAtCorners. (In Flash CS3, the breakAtCorners property was deprecated in favor of [stroke.joinType](/Stroke_object/stroke11.md).) Other properties can be set, depending on the value of the [stroke.style](/Stroke_object/stroke20.md) property.

#### Property summary

The following properties are available for the Stroke object:

| **Property**                                    | **Description**                                                                                         |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [stroke.breakAtCorners](/Stroke_object/stroke.md) | A Boolean value, same as the Sharp Corners setting in the custom Stroke Style dialog box.               |
| [stroke.capType](/Stroke_object/stroke1.md)                 | A string that specifies the type of cap for the stroke.                                                 |
| [stroke.color](/Stroke_object/stroke2.md)                   | A string, hexadecimal value, or integer that represents the stroke color.                               |
| [stroke.curve](/Stroke_object/stroke3.md)                   | A string that specifies the type of hatching for the stroke.                                            |
| [stroke.dash1](/Stroke_object/stroke4.md)                   | An integer that specifies the lengths of the solid part of a dashed line.                               |
| [stroke.dash2](/Stroke_object/stroke5.md)                   | An integer that specifies the lengths of the blank part of a dashed line.                               |
| [stroke.density](/Stroke_object/stroke6.md)                 | A string that specifies the density of a stippled line.                                                 |
| [stroke.dotSize](/Stroke_object/stroke7.md)                 | A string that specifies the dot size of a stippled line.                                                |
| [stroke.dotSpace](/Stroke_object/stroke8.md)                | An integer that specifies the spacing between dots in a dotted line.                                    |
| [stroke.hatchThickness](/Stroke_object/stroke9.md)          | A string that specifies the thickness of a hatch line.                                                  |
| [stroke.jiggle](/Stroke_object/stroke10.md)                  | A string that specifies the jiggle property of a hatched line.                                          |
| [stroke.joinType](/Stroke_object/stroke11.md)                | A string that specifies the type of join for the stroke.                                                |
| [stroke.length](/Stroke_object/stroke12.md)                  | A string that specifies the length of a hatch line.                                                     |
| [stroke.miterLimit](/Stroke_object/stroke13.md)              | A float value that specifies the angle above which the tip of the miter will be truncated by a segment. |
| [stroke.pattern](/Stroke_object/stroke14.md)                 | A string that specifies the pattern of a ragged line.                                                   |
| [stroke.rotate](/Stroke_object/stroke15.md)                  | A string that specifies the rotation of a hatch line.                                                   |
| [stroke.scaleType](/Stroke_object/stroke16.md)               | A string that specifies the type of scale to be applied to the stroke.                                  |

| **Property**                          | **Description**                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------|
| [stroke.shapeFill](/Stroke_object/stroke17.md)     | A [Fill object](/Fill_object/fill_summary.md) that represents the fill settings of the stroke. |
| [stroke.space](/Stroke_object/stroke18.md)         | A string that specifies the spacing of a hatched line.                          |
| [stroke.strokeHinting](/Stroke_object/stroke19.md) | A Boolean value that specifies whether stroke hinting is set on the stroke.     |
| [stroke.style](/Stroke_object/stroke20.md)         | A string that describes the stroke style.                                       |
| [stroke.thickness](/Stroke_object/stroke21.md)     | An integer that specifies the stroke size.                                      |
| [stroke.variation](/Stroke_object/stroke22.md)     | A string that specifies the variation of a stippled line.                       |
| [stroke.waveHeight](/Stroke_object/stroke23.md)    | A string that specifies the wave height of a ragged line.                       |
| [stroke.waveLength](/Stroke_object/stroke24.md)    | A string that specifies the wave length of a ragged line.                       |

<span id="stroke.breakAtCorners" class="anchor"></span>



## swfPanel object

#### Availability

Flash CS4 Professional.

#### Description

The swfPanel object represents a Window SWF panel. Window SWF panels are SWF files that implement applications you can run from the Flash authoring environment; they are available from the Window > Other Panels menu. By default, Window SWF panels are stored in a subfolder of the Configuration folder (see ["Saving JSFL files"](/Introduction/Working_with_the_JavaScript_API.md#saving-jsfl-files)). For example, on Windows XP, the folder is in *boot drive*\\Documents and Settings\\*user*\\Local Settings\\Application Data\\Adobe\\Flash CS4\\*language*\\Configuration\\WindowSWF. A sample Window SWF panel is available; see ["Sample Trace Bitmap panel"](/Introduction/Sample_implementations.md#sample-trace-bitmap-panel). The array of registered Window SWF panels is stored in the [fl.swfPanels](/flash_object_(fl)/fl74.md) property.

#### Method summary

You can use the following method with the swfPanel object:

| **Method**                           | **Description**                                                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [swfPanel.call()](/swfPanel_object/swfPanel.md)  | Works in conjunction with the ActionScript ExternalInterface.addCallback() and MMExecute() methods to communicate with the SWF panel from the authoring environment. |
| [swfPanel.reload()](/swfPanel_object/swfPane5.md)   | Reloads content in the SWF panel.                                                                                                                                    |
| [swfPanel.setFocus()](/swfPanel_object/swfPane6.md) | Sets the keyboard focus to the specified SWF panel.                                                                                                                  |

#### Property summary

You can use the following properties with the swfPanel object:

| **Property**                              | **Description**                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------|
| [swfPanel.dpiScaleFactorX](/swfPanel_object/swfPane1.md) | A string that contains the DPI scale factor (scaleX) for swfPanel.                                   |
| [swfPanel.dpiScaleFactorY](/swfPanel_object/swfPane2.md) | A string that contains the DPI scale factor (scaleY) for swfPanel.                                   |
| [swfPanel.name](/swfPanel_object/swfPane3.md)            | Read-only; a string that represents the name of the specified Window SWF panel.                      |
| [swfPanel.path](/swfPanel_object/swfPane4.md)            | Read-only; a string that represents the path to the SWF file used in the specified Window SWF panel. |

<span id="swfPanel.call()" class="anchor"></span>



## SymbolInstance object


**Inheritance** [Element object](/Element_object/element_summary.md) >[Instance object](/Instance_object/instance_summary.md) >SymbolInstance object

#### Availability

Flash MX 2004.

#### Description

SymbolInstance is a subclass of the Instance object and represents a symbol in a frame (see [Instance object](/Instance_object/instance_summary.md)).

#### Property summary

In addition to the Instance object properties, the SymbolInstance object has the following properties:

<table><thead><tr class="header"><th><strong>Property</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstance.md">symbolInstance.accName</a></td><td>A string that is equivalent to the Name field in the Accessibility panel.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstanc1.md">symbolInstance.actionScript -</a<a href="#_bookmark917">dropped</a></td><td>Dropped in Adobe Animate.</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstanc2.md">symbolInstance.backgroundColor</a></td><td>A string specifying the matte color when Opaque is selected.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstanc3.md">symbolInstance.bitmapRenderMode</a></td><td>A string specifying the display type for a symbol instance.</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstanc4.md">symbolInstance.blendMode</a></td><td>A string that specifies the blending mode to be applied to a movie clip symbol.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstanc5.md">symbolInstance.brightness</a></td><td>An integer that returns the value set in the color effect Property Inspector for brightness (percentage between -100 and 100) when colorMode == 'brightness'.</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstanc6.md">symbolInstance.buttonTracking</a></td><td>A string (button symbols only) that sets the same property as the pop-up menu for Track as Button or Track As Menu Item in the Property inspector.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstanc7.md">symbolInstance.cacheAsBitmap</a></td><td>A Boolean value that specifies whether run-time bitmap caching is enabled.</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstanc8.md">symbolInstance.colorAlphaAmount</a></td><td>An integer that is part of the color transformation for the instance, specifying the Advanced Effect Alpha settings; equivalent to using the Color &gt; Advanced setting in the Property inspector and adjusting the controls on the right of the dialog box.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstanc9.md">symbolInstance.colorAlphaPercent</a></td><td>An integer that specifies part of the color transformation for the instance; equivalent to using the Color &gt; Advanced setting in the instance Property inspector (the percentage controls on the left of the dialog box).</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan10.md">symbolInstance.colorBlueAmount</a></td><td>An integer that is part of the color transformation for the instance; equivalent to using the Color &gt; Advanced setting in the instance Property inspector.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstan11.md">symbolInstance.colorBluePercent</a></td><td>An integer that is part of the color transformation for the instance; equivalent to using the Color &gt; Advanced setting in the instance Property inspector (the percentage controls on the left of the dialog box).</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan12.md">symbolInstance.colorGreenAmount</a></td><td><p>An integer that is part of the color transformation for the instance; equivalent to using the Color&gt;Advanced setting in the instance Property inspector.</p><p>Allowable values are from -255 to 255.</p></td></tr></tbody></table>

<table><thead><tr class="header"><th><strong>Property</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan13.md">symbolInstance.colorGreenPercent</a></td><td><p>Part of the color transformation for the instance;equivalent to using the Color&gt;Advanced setting in the instance Property inspector (the percentage controls on the left of the dialog box).</p></td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstan14.md">symbolInstance.colorMode</a></td><td>A string that specifies the color mode as identified in the symbol Property inspector Color pop-up menu.</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan15.md">symbolInstance.colorRedAmount</a></td><td>An integer that is part of the color transformation for the instance, equivalent to using the Color&gt;Advanced setting in the instance Property inspector.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstan16.md">symbolInstance.colorRedPercent</a></td><td><p>Part of the color transformation for the instance;equivalent to using the Color</p><p>&gt;Advanced setting in the instance Property inspector (the percentage controls on the left of the dialog box).</p></td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan17.md">symbolInstance.description</a></td><td>A string that is equivalent to the Description field in the Accessibility panel.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstan18.md">symbolInstance.filters</a></td><td>An array of Filter objects (see <a href="/Filter_object/filter_summary.md">Filter object</a>).</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan19.md">symbolInstance.firstFrame</a></td><td>A zero-based integer that specifies the first frame to appear in the timeline of the graphic.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstan20.md">symbolInstance.forceSimple</a></td><td>A Boolean value that enables and disables the accessibility of the object’s children; equivalent to the inverse logic of the Make Child Objects Accessible setting in the Accessibility panel.</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan21.md">symbolInstance.is3D</a></td><td>A Boolean value indicating whether the instance contains any 3D transforms.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstan22.md">symbolInstance.loop</a></td><td>A string that, for graphic symbols, sets the same property as the Loop pop-up menu in the Property inspector.</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan23.md">symbolInstance.shortcut</a></td><td>A string that is equivalent to the shortcut key associated with the symbol; equivalent to the Shortcut field in the Accessibility panel.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstan24.md">symbolInstance.silent</a></td><td>A Boolean value that enables or disables the accessibility of the object; equivalent to the inverse logic of the Make Object Accessible setting in the Accessibility panel.</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan25.md">symbolInstance.symbolType</a></td><td>A string that specifies the type of symbol; equivalent to the value for Behavior in the Create New Symbol and Convert To Symbol dialog boxes.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstan26.md">symbolInstance.tabIndex</a></td><td>An integer that is equivalent to the Tab index field in the Accessibility panel.</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan27.md">symbolInstance.tintColor</a></td><td>When the Color Effect Property Inspector is using style tint (colorMode == 'tint'), return the color applied to the tint.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstan28.md">symbolInstance.tintPercent</a></td><td>When the color effect Property Inspector is using style tint (colorMode == 'tint') then return the applied to the tint percentage from -100 to 100.</td></tr><tr class="odd"><td><a href="/SymbolInstance_object/symbolInstan29.md">symbolInstance.useBackgroundColor</a></td><td>A boolean value that specifies whether to use 24 bit mode or 32 bit mode with alpha for the instance.</td></tr><tr class="even"><td><a href="/SymbolInstance_object/symbolInstan30.md">symbolInstance.visible</a></td><td>A boolean value specifying whether the instance is visible or not.</td></tr></tbody></table>

<span id="symbolInstance.accName" class="anchor"></span>



## SymbolItem object


**Inheritance** [Item object](/Item_object/item_summary.md) > SymbolItem object

#### Availability

Flash MX 2004.

#### Description

The SymbolItem object is a subclass of the [Item object](/Item_object/item_summary.md).

#### Method summary

In addition to the Item object methods, you can use the following methods with the SymbolItem object:

| **Method**                                                                | **Description**                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [symbolItem.convertToCompiledClip()](/SymbolItem_object/symbolItem.md) | Converts a symbol item in the library to a compiled movie clip. |
| [symbolItem.exportSWC()](/SymbolItem_object/symbolIte1.md)                                   | Exports the symbol item to a SWC file.                          |
| [symbolItem.exportSWF()](/SymbolItem_object/symbolIte2.md)                                   | Exports the symbol item to a SWF file.                          |
| [symbolItem.exportToLibrary()](/SymbolItem_object/symbolIte3.md)                             | Export an instance to a new bitmap in the Library.              |
| [symbolItem.exportToPNGSequence()](/SymbolItem_object/symbolIte4.md)                         | Export a symbol to a sequence of PNG files.                     |

#### Property summary

In addition to the Item object properties, the following properties are available for the SymbolItem object:

| **Property**                                  | **Description**                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------|
| [symbolItem.lastModifiedDate](/SymbolItem_object/symbolIte5.md)  | A string hexadecimal value that indicates the modification date of the symbol.             |
| [symbolItem.scalingGrid](/SymbolItem_object/symbolIte6.md)       | A Boolean value that specifies whether 9-slice scaling is enabled for the item.            |
| [symbolItem.scalingGridRect](/SymbolItem_object/symbolIte7.md)   | A Rectangle object that specifies the locations of the four 9-slice guides.                |
| [symbolItem.sourceAutoUpdate](/SymbolItem_object/symbolIte8.md)  | A Boolean value that specifies whether the item is updated when the FLA file is published. |
| [symbolItem.sourceFilePath](/SymbolItem_object/symbolIte9.md)    | A string that specifies the path for the source FLA file as a file:/// URI.                |
| [symbolItem.sourceLibraryName](/SymbolItem_object/symbolIt10.md) | A string that specifies the name of the item in the source file library.                   |
| [symbolItem.symbolType](/SymbolItem_object/symbolIt11.md)        | A string that specifies the type of symbol.                                                |
| [symbolItem.timeline](/SymbolItem_object/symbolIt12.md)          | Read-only; a [Timeline object](/Timeline_object/timeline_summary.md).                                            |

<span id="symbolItem.convertToCompiledClip()" class="anchor"></span>



## Text Object


**Inheritance** [Element object](/Element_object/element_summary.md) > Text object

#### Availability

Flash MX 2004.

#### Description

The Text object represents a single text item in a document. All properties of the text pertain to the entire text block.

To set properties of a text run within the text field, see the Property summary for the [TextAttrs object](/TextAttrs_object/textAttrs_summary.md). To change properties of a selection within a text field, you can use [document.setElementTextAttr()](/Document_object/docum500.md) and specify a range of text, or use the current selection.

To set generic properties of the selected text field, use [document.setElementProperty()](/Document_object/docum490.md). The following example sets the x value of the selected text field's registration point to 50:

 fl.getDocumentDOM().setElementProperty("x", 50); 

#### Method summary

In addition to the Element object methods, the following methods are available for the Text object:

| **Method**                            | **Description**                                                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [text.getTextAttr()](/Text_object/text11.md)   | Retrieves the specified attribute for the text identified by the optional ***startIndex*** and ***endIndex*** parameters. |
| [text.getTextString()](/Text_object/text12.md) | Retrieves the specified range of text.                                                                                    |
| [text.setTextAttr()](/Text_object/text22.md)   | Sets the specified attribute associated with the text identified by ***startIndex*** and ***endIndex***.                  |
| [text.setTextString()](/Text_object/text23.md) | Changes the text string within this Text object.                                                                          |

#### Property summary

In addition to the Element object properties, the following properties are available for the Text object:

| **Property**                             | **Description**                                                                                                                                      |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [text.accName](/Text_object/text.md)            | A string that is equivalent to the Name field in the Accessibility panel.                                                                            |
| [text.antiAliasSharpness](/Text_object/text1.md) | A float value that specifies the anti-aliasing sharpness of the text.                                                                                |
| [text.antiAliasThickness](/Text_object/text2.md) | A float value that specifies the anti-aliasing thickness of the text.                                                                                |
| [text.autoExpand](/Text_object/text3.md)         | A Boolean value that controls the expansion of the bounding width for static text fields or the bounding width and height for dynamic or input text. |
| [text.border](/Text_object/text4.md)             | A Boolean value that controls whether Flash shows (true) or hides (false) a border around dynamic or input text.                                     |
| [text.description](/Text_object/text5.md)        | A string that is equivalent to the Description field in the Accessibility panel.                                                                     |

<table><thead><tr class="header"><th><strong>Property</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/Text_object/text6.md">text.embeddedCharacters</a></td><td>A string that specifies characters to embed. This is equivalent to entering text in the Character Embedding dialog box.</td></tr><tr class="even"><td><a href="/Text_object/text7.md">text.embedRanges</a></td><td>A string that consists of delimited integers that correspond to the items that can be selected in the Character Embedding dialog box.</td></tr><tr class="odd"><td><a href="/Text_object/text8.md">text.embedVariantGlyphs</a></td><td>A Boolean value that specifies whether to enable the embedding of variant glyphs.</td></tr><tr class="even"><td><a href="/Text_object/text9.md">text.filters</a></td><td>An array of filters applied to the text element</td></tr><tr class="odd"><td><a href="/Text_object/text10.md">text.fontRenderingMode</a></td><td>A string that specifies the rendering mode for the text.</td></tr><tr class="even"><td><a href="/Text_object/text13.md">text.length</a></td><td>Read-only; an integer that represents the number of characters in the Text object.</td></tr><tr class="odd"><td><a href="/Text_object/text14.md">text.lineType</a></td><td><p>A string that sets the line type to "single line", "multiline", "multiline no wrap", or</p><p>"password".</p></td></tr><tr class="even"><td><a href="/Text_object/text15.md">text.maxCharacters</a></td><td>An integer that specifies the maximum characters the user can enter into this Text object.</td></tr><tr class="odd"><td><a href="/Text_object/text16.md">text.orientation</a></td><td>A string that specifies the orientation of the text field.</td></tr><tr class="even"><td><a href="/Text_object/text17.md">text.renderAsHTML</a></td><td>A Boolean value that controls whether Flash draws the text as HTML and interprets embedded HTML tags.</td></tr><tr class="odd"><td><a href="/Text_object/text18.md">text.scrollable</a></td><td>A Boolean value that controls whether the text can (true) or cannot (false) be scrolled.</td></tr><tr class="even"><td><a href="/Text_object/text19.md">text.selectable</a></td><td>A Boolean value that controls whether the text can (true) or cannot (false) be selected. Input text is always selectable.</td></tr><tr class="odd"><td><a href="/Text_object/text20.md">text.selectionEnd</a></td><td>A zero-based integer that specifies the offset of the end of a text subselection.</td></tr><tr class="even"><td><a href="/Text_object/text21.md">text.selectionStart</a></td><td>A zero-based integer that specifies the offset of the beginning of a text subselection.</td></tr><tr class="odd"><td><a href="/Text_object/text24.md">text.shortcut</a></td><td>A string that is equivalent to the Shortcut field in the Accessibility panel.</td></tr><tr class="even"><td><a href="/Text_object/text25.md">text.silent</a></td><td>A Boolean value that specifies whether the object is accessible.</td></tr><tr class="odd"><td><a href="/Text_object/text26.md">text.tabIndex</a></td><td>An integer that is equivalent to the Tab Index field in the Accessibility panel.</td></tr><tr class="even"><td><a href="/Text_object/text27.md">text.textRuns</a></td><td>Read-only; an array of TextRun objects.</td></tr><tr class="odd"><td><a href="/Text_object/text28.md">text.textType</a></td><td><p>A string that specifies the type of text field. Acceptable values are "static", "dynamic", and</p><p>"input".</p></td></tr><tr class="even"><td><a href="/Text_object/text29.md">text.useDeviceFonts</a></td><td>A Boolean value. A value of true causes Flash to draw text using device fonts.</td></tr><tr class="odd"><td><a href="/Text_object/text30.md">text.variableName</a></td><td>A string that contains the contents of the Text object.</td></tr></tbody></table>

<span id="text.accName" class="anchor"></span>


## TextAttrs Object

#### Availability

Flash MX 2004.

#### Description

The TextAttrs object contains all the properties of text that can be applied to a subselection. This object is a property of the TextRun object ([textRun.textAttrs](/TextRun_object/textRun.md)).

#### Property summary

The following properties are available for the TextAttrs object:

| **Property**                                  | **Description**                                                                                                                        |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [textAttrs.aliasText](/TextAttrs_object/textAttrs.md)   | A Boolean value that specifies that Flash should draw the text using a method optimized for increasing the legibility of small text.   |
| [textAttrs.alignment](/TextAttrs_object/textAttr1.md)         | A string that specifies paragraph justification. Acceptable values are "left", "center", "right", and "justify".                       |
| [textAttrs.autoKern](/TextAttrs_object/textAttr2.md)          | A Boolean value that determines whether Flash uses (true) or ignores (false) pair kerning information in the font(s) to kern the text. |
| [textAttrs.bold](/TextAttrs_object/textAttr3.md)              | A Boolean value. A value of true causes text to appear with the bold version of the font.                                              |
| [textAttrs.characterPosition](/TextAttrs_object/textAttr4.md) | A string that determines the baseline for the text.                                                                                    |
| [textAttrs.characterSpacing](/TextAttrs_object/textAttr5.md)  | Deprecated in favor of [textAttrs.letterSpacing](/TextAttrs_object/textAtt11.md). An integer that represents the space between characters.             |
| [textAttrs.face](/TextAttrs_object/textAttr6.md)              | A string that represents the name of the font, such as "Arial".                                                                        |
| [textAttrs.fillColor](/TextAttrs_object/textAttr7.md)         | A string, hexadecimal value, or integer that represents the fill color.                                                                |
| [textAttrs.indent](/TextAttrs_object/textAttr8.md)            | An integer that specifies paragraph indentation.                                                                                       |
| [textAttrs.italic](/TextAttrs_object/textAttr9.md)            | A Boolean value. A value of true causes text to appear with the italic version of the font.                                            |
| [textAttrs.leftMargin](/TextAttrs_object/textAtt10.md)        | An integer that specifies the paragraph’s left margin.                                                                                 |
| [textAttrs.letterSpacing](/TextAttrs_object/textAtt11.md)     | An integer that represents the space between characters.                                                                               |
| [textAttrs.lineSpacing](/TextAttrs_object/textAtt12.md)       | An integer that specifies the line spacing (leading) of the paragraph                                                                  |
| [textAttrs.rightMargin](/TextAttrs_object/textAtt13.md)       | An integer that specifies the paragraph’s right margin.                                                                                |
| [textAttrs.rotation](/TextAttrs_object/textAtt14.md)          | A Boolean value. A value of true causes Flash to rotate the characters of the text 90°. The default value is false.                    |
| [textAttrs.size](/TextAttrs_object/textAtt15.md)              | An integer that specifies the size of the font.                                                                                        |
| [textAttrs.target](/TextAttrs_object/textAtt16.md)            | A string that represents the target property of the text field.                                                                        |
| [textAttrs.url](/TextAttrs_object/textAtt17.md)               | A string that represents the URL property of the text field.                                                                           |

<span id="textAttrs.aliasText" class="anchor"></span>



## TextRun Object


#### Availability

Flash MX 2004.

#### Description

The TextRun object represents a run of characters that have attributes that match all of the properties in the [TextAttrs object](/TextAttrs_object/textAttrs_summary.md) . This object is a property of the Text object ([text.textRuns](/Text_object/text27.md)).

#### Property summary

In addition to the properties available for use with the Text object, the TextRun object provides the following properties:

| **Property**                            | **Description**                                                    |
|-----------------------------------------|--------------------------------------------------------------------|
| [textRun.characters](/TextRun_object/textRun1.md)    | A string that represents the text contained in the TextRun object. |
| [textRun.textAttrs](/TextRun_object/textRun.md) | The TextAttrs object containing the attributes of the run of text. |

<span id="textRun.textAttrs" class="anchor"></span>



## TextureAtlasExporter object


**Inheritance** [Item object](/Item_object/item_summary.md) >TextureAtlasExporter object

#### Availability

Animate 2020.

#### Description

The TextureAtlasExporter object is a subclass of the [Item object](/Item_object/item_summary.md).

#### Method summary

In addition to the Item object methods, you can use the following methods with the TextureAtlasExporter object:

| **Method**                                                          | **Description**                                                   |
|---------------------------------------------------------------------|-------------------------------------------------------------------|
| [TextureAtlasExporter.exportTextureAtlas()](/TextureAtlasExporter_object/TextureAtlasExporter.md)| Exports the texture atlas for the selected symbol. |

#### Property summary

In addition to the Item object properties, the following properties are available for the SpriteSheetExporter object:

| **Property**                                       | **Description**                                                                                                          |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [TextureAtlasExporter.algorithm](/TextureAtlasExporter_object/TextureAtlasExporter1.md)     | Sets the encoding algorithm for the TextureAtlas                                |
| [TextureAtlasExporter.allowRotate](/TextureAtlasExporter_object/TextureAtlasExporter2.md)   | Allows sprites to be rotated when added to the TextureAtlas                                       
| [TextureAtlasExporter.app](/TextureAtlasExporter_object/TextureAtlasExporter3.md)           | A string indicating the name of the application that is generating the TextureAtlas.                                             |
| [TextureAtlasExporter.autoSize](/TextureAtlasExporter_object/TextureAtlasExporter4.md)      | A boolean value indicating whether the TextureAtlasExporter should calculate the overall size of TextureAtlas on its own.                                                                  |
| [TextureAtlasExporter.borderPadding](/TextureAtlasExporter_object/TextureAtlasExporter5.md) | An integer indicating the number of pixels of padding to add around each texture in the texture atlas.        
| [TextureAtlasExporter.canRotate](/TextureAtlasExporter_object/TextureAtlasExporter6.md)     | A boolean value indicating whether the framework specified by the TextureAtlasExporter.layoutFormat property may rotate textures when adding them to the texture atlas. |
| [TextureAtlasExporter.filePath](/TextureAtlasExporter_object/TextureAtlasExporter7.md)   | It's the location where the texture atlas files needs to be exported.    |
| [TextureAtlasExporter.flattenSkewObject](/TextureAtlasExporter_object/TextureAtlasExporter8.md)   | It's the location where the texture atlas files needs to be exported.    |
| [TextureAtlasExporter.imageFormat](/TextureAtlasExporter_object/TextureAtlasExporter9.md)   | Boolean value which indicates whether skewed assets needs to be flattened to the texture atlas..    |
| [TextureAtlasExporter.optimizeBitmap](/TextureAtlasExporter_object/TextureAtlasExporter10.md)   | Boolean value which indicates whether texture atlas bitmaps needs to be optimized by removing extra spaces.    |
| [TextureAtlasExporter.optimizeJson](/TextureAtlasExporter_object/TextureAtlasExporter11.md)   |  Boolean value which indicates whether animation.json needs to be optimized by removing indentation, decomposed matrix and use shortened names.    |
| [TextureAtlasExporter.overflowed](/TextureAtlasExporter_object/TextureAtlasExporter12.md)   | Read-only property; Boolean value which indicates, if any assets are remaining after packing into texture atlas.    |
| [TextureAtlasExporter.resolution](/TextureAtlasExporter_object/TextureAtlasExporter13.md)   | Floating value which indicates in which resolution the textures needs to be exported.    |
| [TextureAtlasExporter.shapePadding](/TextureAtlasExporter_object/TextureAtlasExporter14.md)   | An integer value indicating how many pixels of padding should be added to each exported symbol frame when adding it to the TextureAtlas.    |
| [TextureAtlasExporter.sheetHeight](/TextureAtlasExporter_object/TextureAtlasExporter15.md)   | An integer value specifying the height of the texture atlas. This value is read-only if TextureAtlasExporter.autoSize is set to true..    |
| [TextureAtlasExporter.sheetWidth](/TextureAtlasExporter_object/TextureAtlasExporter16.md)   | An integer value specifying the width of the texture atlas. This value is read-only if TextureAtlasExporter.autoSize is set to true.    |
| [TextureAtlasExporter.version](/TextureAtlasExporter_object/TextureAtlasExporter17.md)   | Read-only property; A stinrg indicating the version number of the Animate application. This property is provided for use by texture atlas plugins.    |



## Timeline Object


#### Availability

Flash MX 2004.

#### Description

The Timeline object represents the Animate timeline, which can be accessed for the current document by using fl.getDocumentDOM().getTimeline(). This method returns the timeline of the current scene or symbol that is being edited.
When you work with scenes, each scene’s timeline has an index value, and can be accessed for the current document by fl.getDocumentDOM().timelines[i]. (In this example, i is the index of the value of the timeline.)
When you work with frames by using the methods and properties of the Timeline object, remember that the frame value is a zero-based index (not the actual frame number in the sequence of frames in the timeline). That is, the first frame has a frame index of 0.

#### Method summary

The following methods are available for the Timeline object:

| **Method**                                              | **Description**                                                                                                                                                                            |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [timeline.addMotionGuide()](/Timeline_object/timeline.md) | Adds a motion guide layer above the current layer and attaches the current layer to the newly added guide layer.                                                                           |
| [timeline.addNewLayer()](/Timeline_object/timelin1.md)                | Adds a new layer to the document and makes it the current layer.                                                                                                                           |
| [timeline.clearFrames()](/Timeline_object/timelin2.md)                | Deletes all the contents from a frame or range of frames on the current layer.                                                                                                             |
| [timeline.clearKeyframes()](/Timeline_object/timelin3.md)             | Converts a keyframe to a regular frame and deletes its contents on the current layer.                                                                                                      |
| [timeline.convertToBlankKeyframes()](/Timeline_object/timelin4.md)    | Converts frames to blank keyframes on the current layer.                                                                                                                                   |
| [timeline.convertToKeyframes()](/Timeline_object/timelin5.md)         | Converts a range of frames to keyframes (or converts the selection if no frames are specified) on the current layer.                                                                       |
| [timeline.copyFrames()](/Timeline_object/timelin6.md)                 | Copies a range of frames on the current layer to the clipboard.                                                                                                                            |
| [timeline.copyLayers()](/Timeline_object/timelin7.md)                 | Copies a range of Timeline layers to the clipboard.                                                                                                                                        |
| [timeline.copyMotion()](/Timeline_object/timelin8.md)                 | Copies motion on selected frames, either from a motion tween or from frame-by-frame animation, so it can be applied to other frames.                                                       |
| [timeline.copyMotionAsAS3()](/Timeline_object/timelin9.md)            | Copies motion on selected frames, either from a motion tween or from frame-by-frame animation, to the clipboard as ActionScript 3.0 code.                                                  |
| [timeline.createMotionObject()](/Timeline_object/timeli10.md)         | Creates a new motion object at a designated start and end frame.                                                                                                                           |
| [timeline.createMotionTween()](/Timeline_object/timeli11.md)          | Sets the [frame.tweenType](/Frame_object/frame39.md) property to motion for each selected keyframe on the current layer, and converts each frame’s contents to a single symbol instance if necessary. |

<table><thead><tr class="header"><th><strong>Method</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="/Timeline_object/timeli14.md">timeline.cutFrames()</a></td><td>Cuts a range of frames on the current layer from the timeline and saves them to the clipboard.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli15.md">timeline.cutLayers()</a></td><td>Cuts a range of Timeline layers and saves them to the clipboard.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli16.md">timeline.deleteLayer()</a></td><td>Deletes a layer.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli17.md">timeline.duplicateLayers()</a></td><td>Duplicates the selected layers or specified layers.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli18.md">timeline.expandFolder()</a></td><td>Expands or collapses the specified folder or folders.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli19.md">timeline.findLayerIndex()</a></td><td>Finds an array of indexes for the layers with the given name.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli21.md">timeline.getBounds()</a></td><td>Returns the bounding rectangle for all elements on all layers on the Timeline, for a given frame.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli22.md">timeline.getFrameProperty()</a></td><td>Retrieves the specified property’s value for the selected frames.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli23.md">timeline.getGuidelines()</a></td><td>Returns an XML string that represents the current positions of the horizontal and vertical guide lines for a timeline (View &gt; Guides &gt; Show Guides).</td></tr><tr class="even"><td><a href="/Timeline_object/timeli24.md">timeline.getLayerProperty()</a></td><td>Retrieves the specified property’s value for the selected layers.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli25.md">timeline.getSelectedFrames()</a></td><td>Retrieves the currently selected frames in an array.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli26.md">timeline.getSelectedLayers()</a></td><td>Retrieves the zero-based index values of the currently selected layers.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli27.md">timeline.insertBlankKeyframe()</a></td><td>Inserts a blank keyframe at the specified frame index; if the index is not specified, inserts the blank keyframe by using the playhead/selection.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli28.md">timeline.insertFrames()</a></td><td>Inserts the specified number of frames at the given frame number.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli29.md">timeline.insertKeyframe()</a></td><td>Inserts a keyframe at the specified frame.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli51.md">timeline.mergeLayers()</a></td><td> Merge the layers within a specified range of indexes.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli34.md">timeline.pasteFrames()</a></td><td>Pastes the range of frames from the clipboard into the specified frames.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli35.md">timeline.pasteLayers()</a></td><td>Pastes copied layers to the Timeline above the specified layer index.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli36.md">timeline.pasteMotion()</a></td><td><p>Pastes the range of motion frames retrieved by</p><p>timeline.copyMotion() to the Timeline.</p></td></tr><tr class="odd"><td><a href="/Timeline_object/timeli37.md">timeline.pasteMotionSpecial()</a></td><td>Pastes motion on selected frames, displaying a dialog box that lets the user choose which parts of a classic tween to paste.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli38.md">timeline.removeFrames()</a></td><td>Deletes the frame.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli39.md">timeline.removeMotionObject()</a></td><td>Removes the motion object created with timeline.createMotionObject(), and converts the frame(s) to static frames.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli40.md">timeline.reorderLayer()</a></td><td>Moves the first specified layer before or after the second specified layer.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli41.md">timeline.reverseFrames()</a></td><td>Reverses a range of frames.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli42.md">timeline.selectAllFrames()</a></td><td>Selects all the frames in the current timeline.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli43.md">timeline.setFrameProperty()</a></td><td>Sets the property of the Frame object for the selected frames.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli44.md">timeline.setGuidelines()</a></td><td>Replaces the guide lines for the timeline with the information specified.</td></tr><tr class="odd"><td><a href="/Timeline_object/timeli45.md">timeline.setLayerProperty()</a></td><td>Sets the specified property on all the selected layers to a specified value.</td></tr><tr class="even"><td><a href="/Timeline_object/timeli46.md">timeline.setSelectedFrames()</a></td><td>Selects a range of frames in the current layer or sets the selected frames to the selection array passed into this method.</td></tr></tbody></table>

| **Method**                                     | **Description**                                                                  |
|------------------------------------------------|----------------------------------------------------------------------------------|
| [timeline.setSelectedLayers()](/Timeline_object/timeli47.md) | Sets the layer to be selected; also makes the specified layer the current layer. |
| [timeline.showLayerMasking()](/Timeline_object/timeli48.md)  | Shows the layer masking during authoring by locking the mask and masked layers.  |
| [timeline.startPlayback()](/Timeline_object/timeli49.md)     | Starts automatic playback of the timeline if it is not currently playing.        |
| [timeline.stopPlayback()](/Timeline_object/timeli50.md)      | Stops autoumatic playback of the timeline if it is currently playing.            |

#### Property summary

The following properties are available for the Timeline object:

| **Property**                            | **Description**                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------|
| [timeline.advancedLayersEnabled](/Timeline_object/timeli52.md)         | Enable / disable advanced layers mode. |
| [timeline.currentFrame](/Timeline_object/timeli12.md) | A zero-based index for the frame at the current playhead location.                           |
| [timeline.currentLayer](/Timeline_object/timeli13.md) | A zero-based index for the currently active layer.                                           |
| [timeline.frameCount](/Timeline_object/timeli20.md)   | Read-only; an integer that represents the number of frames in this timeline’s longest layer. |
| [timeline.layerCount](/Timeline_object/timeli30.md)   | Read-only; an integer that represents the number of layers in the specified timeline.        |
| [timeline.layers](/Timeline_object/timeli31.md)       | Read-only; an array of layer objects.                                                        |
| [timeline.libraryItem](/Timeline_object/timeli32.md)  | Read-only property; indicates whether the timeline belongs to a scene.                       |
| [timeline.name](/Timeline_object/timeli33.md)         | A string that represents the name of the current timeline.                                   |


<span id="timeline.addMotionGuide()" class="anchor"></span>



## ToolObj object


#### Availability

Flash MX 2004.

#### Description

A ToolObj object represents an individual tool in the Tools panel. To access a ToolObj object, use properties of the [Tools object](/Tools_object/tools_summary.md): either the [tools.toolObjs](/Tools_object/tools11.md) array or [tools.activeTool](/Tools_object/tools.md).

#### Method summary

The following methods are available for the ToolObj object.

***Note:** The following methods are used only when creating extensible tools.*

| **Method**                                       | **Description**                                                                                                                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [toolObj.enablePIControl()](/ToolObj_object/toolObj1.md)      | Enables or disables the specified control in a Property inspector. Used only when creating extensible tools.                                                                    |
| [toolObj.setIcon()](/ToolObj_object/toolObj4.md)              | Identifies a PNG file to use as a tool icon in the Flash Tools panel.                                                                                                           |
| [toolObj.setMenuString()](/ToolObj_object/toolObj5.md)        | Sets the string that appears in the pop-up menu as the name for the tool.                                                                                                       |
| [toolObj.setOptionsFile()](/ToolObj_object/toolObj6.md)       | Associates an XML file with the tool.                                                                                                                                           |
| [toolObj.setPI()](/ToolObj_object/toolObj7.md)                | Sets a particular Property inspector to be used when the tool is activated.                                                                                                     |
| [toolObj.setToolName()](/ToolObj_object/toolObj8.md)          | Assigns a name to the tool for the configuration of the Tools panel.                                                                                                            |
| [toolObj.setToolTip()](/ToolObj_object/toolObj9.md)           | Sets the tooltip that appears when the mouse is held over the tool icon.                                                                                                        |
| [toolObj.showPIControl()](/ToolObj_object/toolOb10.md)        | Shows or hides a control in the Property inspector.                                                                                                                             |
| [toolObj.showTransformHandles()](/ToolObj_object/toolOb11.md) | Called in the [configureTool()](/Top-Level_Functions_and_Methods/configureTool.md) method of an extensible tool’s JavaScript file to indicate that the free transform handles should appear when the tool is active. |

#### Property summary

The following properties are available for the ToolObj object:

| **Property**                       | **Description**                                                                        |
|------------------------------------|----------------------------------------------------------------------------------------|
| [toolObj.depth](/ToolObj_object/toolObj.md)    | An integer that specifies the depth of the tool in the pop-up menu in the Tools panel. |
| [toolObj.iconID](/ToolObj_object/toolObj2.md)   | An integer that specifies the resource ID of the tool.                                 |
| [toolObj.position](/ToolObj_object/toolObj3.md) | Read-only; an integer specifying the position of the tool in the Tools panel.          |

<span id="toolObj.depth" class="anchor"></span>



## Tools Object


#### Availability

Flash MX 2004.

#### Description

The Tools object is accessible from the flash object ([fl.tools](/flash_object_(fl)/fl76.md)). The [tools.toolObjs](/Tools_object/tools11.md) property contains an array of ToolObj objects, and the [tools.activeTool](/Tools_object/tools.md) property returns the ToolObj object for the currently active tool. (See also [ToolObj object](/ToolObj_object/toolObj_summary.md) and the list of Extensible tools in ["Top-Level Functions and Methods"](/Top-Level_Functions_and_Methods/Top.md).)

***Note:** The following methods and properties are used only when creating extensible tools.*

#### Method summary

The following methods are available for the Tools object:

| **Method**                               | **Description**                                                                                                   |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [tools.constrainPoint()](/Tools_object/tools2.md) | Takes two points and returns a new adjusted or *constrained* point.                                               |
| [tools.getKeyDown()](/Tools_object/tools4.md)     | Returns the most recently pressed key.                                                                            |
| [tools.setCursor()](/Tools_object/tools8.md)      | Sets the pointer to a specified appearance.                                                                       |
| [tools.snapPoint()](/Tools_object/tools10.md)      | Takes a point as input and returns a new point that may be adjusted or *snapped* to the nearest geometric object. |

#### Property summary

The following properties are available for the Tools object:

| **Property**                          | **Description**                                                                            |
|---------------------------------------|--------------------------------------------------------------------------------------------|
| [tools.activeTool](/Tools_object/tools.md) | Read-only; returns the [ToolObj object](/ToolObj_object/toolObj_summary.md) for the currently active tool.     |
| [tools.altIsDown](/Tools_object/tools1.md)     | Read-only; a Boolean value that identifies if the Alt key is being pressed.                |
| [tools.ctlIsDown](/Tools_object/tools3.md)     | Read-only; a Boolean value that identifies if the Control key is being pressed.            |
| [tools.mouseIsDown](/Tools_object/tools5.md)   | Read-only; a Boolean value that identifies if the left mouse button is currently pressed.  |
| [tools.penDownLoc](/Tools_object/tools6.md)    | Read-only; a point that represents the position of the last mouse-down event on the Stage. |
| [tools.penLoc](/Tools_object/tools7.md)        | Read-only; a point that represents the current location of the mouse.                      |
| [tools.shiftIsDown](/Tools_object/tools9.md)   | Read-only; a Boolean value that identifies if the Shift key is being pressed.              |
| [tools.toolObjs](/Tools_object/tools11.md)      | Read-only; an array of ToolObj objects.                                                    |

<span id="tools.activeTool" class="anchor"></span>



## Tween Object

#### Availability

Flash Pro CC.

#### Description

The Tween object can be used to access interpolated properties of tweens. Accessing properties for a non-tween frame throws errors.

#### Method Summary

You can use the following methods with the Tween object class:

<table>
   <thead>
      <tr class="header">
         <th><strong>Method</strong></th>
         <th>
            <p><strong>Description</strong></p>
         </th>
      </tr>
   </thead>
   <tbody>
      <tr class="odd">
         <td><a href="/Tween_Object/Tween.md">"Tween.getColorTransform( )"</a>
         <td>
            <p>Returns color transformation data between frames.</p>
         </td>
      </tr>
      <tr class="even">
         <td>
            <p><a href="/Tween_Object/Tween1.md">"Tween.getFilters( )"</a>
         <td>
            <p>Returns filters data of a selected frame from a tween span.</p>
         </td>
      </tr>
      <tr class="odd">
         <td><a href="/Tween_Object/Tween2.md">"Tween.getGeometricTransform()"</a>
         <td>
            <p>Returns Matrix object that represents geometric transformation of a tween within a user-defined range (from offset to a selected frame).</p>
         </td>
      </tr>
      <tr class="even">
         <td><a href="/Tween_Object/Tween3.md">"Tween.getShape( )"</a>
         <td>
            <p>Returns interpolated shape of a selected frame within a tween-span.</p>
         </td>
      </tr>
   </tbody>
</table>

#### Properties Summary

You can use the following properties within methods of Tween object class:

<table><thead><tr class="header"><th><strong>Property</strong></th><th><p><strong>Description</strong></p></th></tr></thead><tbody><tr class="odd"><td><a href="/Tween_Object/Tween4.md">"Tween. duration" </a><td><p>Duration of a tween span that is equal to number of frames in a tween.</p></td></tr><tr class="even"><td><a href="/Tween_Object/Tween5.md">"Tween. startFrame" </a><td><p>Start frame of a tween.</p></td></tr><tr class="odd"><td><a href="/Tween_Object/Tween6.md">"Tween. tweenType" </a><td><p>Specifies the type of tween. For example, Motion or Shape.</p></td></tr></tbody></table>

#### Usage

var mat;
var frame = fl.getDocumentDOM().getTimeline().layers[0].frames[0];
var tweenObj = frame.tweenObj;
var frame1 = fl.getDocumentDOM().getTimeline().layers[1].frames[0];
fl.trace(" Tween duration = " + tweenObj.duration);
for(var i = 1; i < tweenObj.duration; i++) {
mat = tweenObj.getGeometricTransform(i);
var colors = tweenObj.getColorTransform(i);
fl.trace(" Frame " + i + " Matrix = a = " + mat.a + " b = " + mat.b + " c = " + mat.c + " d =
" + mat.d + " tx = " + mat.tx + " ty = " + mat.ty );
fl.trace(" color transform :");
fl.trace(" alpha : amount = "+colors.colorAlphaAmount+" percent = "+colors.colorAlphaPercent);
fl.trace(" red : amount = "+colors.colorRedAmount+" percent = "+colors.colorRedPercent);
fl.trace(" green : amount = "+colors.colorGreenAmount+" percent = "+colors.colorGreenPercent);
fl.trace(" blue : amount = "+colors.colorBlueAmount+" percent = "+colors.colorBluePercent); }

<span id="Tween.getColorTransform(_)" class="anchor"></span>



## Vertex object


#### Availability

Flash MX 2004.

#### Description

The Vertex object is the part of the shape data structure that holds the coordinate data.

#### Method summary

You can use the following methods with the Vertex object:

| **Method**                                    | **Description**                                                  |
|-----------------------------------------------|------------------------------------------------------------------|
| [vertex.getHalfEdge()](/Vertex_object/vertex.md) | Gets a [HalfEdge object](/HalfEdge_object/halfEdge_summary.md) that shares this vertex. |
| [vertex.setLocation()](/Vertex_object/vertex1.md)        | Sets the location of the vertex.                                 |

#### Property summary

The following properties are available for the Vertex object:

| **Property**               | **Description**                                      |
|----------------------------|------------------------------------------------------|
| [vertex.x](/Vertex_object/vertex2.md) | Read-only; the *x* location of the vertex in pixels. |
| [vertex.y](/Vertex_object/vertex3.md) | Read-only; the *y* location of the vertex in pixels. |

<span id="vertex.getHalfEdge()" class="anchor"></span>



## VideoItem Object


**Inheritance** [Item object](/Item_object/item_summary.md) > VideoItem object

#### Availability

Flash MX 2004.

#### Description

The VideoItem object is a subclass of the [Item object](/Item_object/item_summary.md).

#### Method summary

In addition to the Item object methods, the VideoItem object has the following method:

| **Property**                                        | **Description**                            |
|-----------------------------------------------------|--------------------------------------------|
| [videoItem.exportToFLV()](/VideoItem_object/videoItem.md) | Exports the specified item to an FLV file. |

#### Property summary

In addition to the Item object properties, you can use the following properties with the VideoItem object:

| **Property**                                     | **Description**                                                                                                                                                                                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [videoItem.fileLastModifiedDate](/VideoItem_object/videoIte1.md) | Read-only; a string containing a hexadecimal number that represents the number of seconds that have elapsed between January 1, 1970, and the modification date of the original file (on disk) at the time the file was imported to the library. |
| [videoItem.lastModifiedDate](/VideoItem_object/videoIte2.md)     | Read-only; the modification date of the video item in the Library.                                                                                                                                                                              |
| [videoItem.sourceFileExists](/VideoItem_object/videoIte3.md)     | Read-only; a Boolean value that specifies whether the file that was imported to the Library still exists in the location from where it was imported.                                                                                            |
| [videoItem.sourceFileIsCurrent](/VideoItem_object/videoIte4.md)  | Read-only; a Boolean value that specifies whether the file modification date of the Library item is the same as the modification date (on disk) of the file that was imported.                                                                  |
| [videoItem.sourceFilePath](/VideoItem_object/videoIte5.md)       | Read-only; a string that specifies the path to the video item.                                                                                                                                                                                  |
| [videoItem.videoType](/VideoItem_object/videoIte6.md)            | Read-only; a string that specifies the type of video the item represents.                                                                                                                                                                       |

<span id="videoItem.exportToFLV()" class="anchor"></span>



## XMLUI Object

#### Availability

Flash MX 2004.

#### Description

Flash 8 supports custom dialog boxes written in a subset of the XML User Interface Language (XUL). An XML User Interface (XMLUI) dialog box can be used by several Flash features, such as commands and behaviors, to provide a user interface for features that you build using extensibility. The XMLUI object provides the ability to get and set properties of an XMLUI dialog box, and accept or cancel out of one. The XMLUI methods can be used in callbacks, such as *oncommand* handlers in buttons.
You can write a dialog.xml file and invoke it from the JavaScript API using the [document.xmlPanel()](/Document_object/docu6198.md) method. To retrieve an object representing the current XMLUI dialog box, use [fl.xmlui](/flash_object_(fl)/fl81.md).

#### Method summary

The following methods are available for the XMLUI object:

| **Method**                                       | **Description**                                                                             |
|--------------------------------------------------|---------------------------------------------------------------------------------------------|
| [xmlui.accept()](/XMLUI_object/xmlui.md)                | Closes the current XMLUI dialog box with an accept state.                                   |
| [xmlui.cancel()](/XMLUI_object/xmlui1.md)                 | Closes the current XMLUI dialog box with a cancel state.                                    |
| [xmlui.get()](/XMLUI_object/xmlui2.md)                    | Retrieves the value of the specified property of the current XMLUI dialog box.              |
| [xmlui.getControlItemElement()](/XMLUI_object/xmlui3.md)  | Returns the current control item for the specified control.                                 |
| [xmlui.getEnabled()](/XMLUI_object/xmlui4.md)             | Returns a Boolean value that specifies whether the control is enabled or disabled (dimmed). |
| [xmlui.getVisible()](/XMLUI_object/xmlui5.md)             | Returns a Boolean value that specifies whether the control is visible or hidden.            |
| [xmlui.set()](/XMLUI_object/xmlui6.md)                    | Modifies the value of the specified property of the current XMLUI dialog box.               |
| [xmlui.setControlItemElement()](/XMLUI_object/xmlui7.md)  | Sets the label and value for the current item.                                              |
| [xmlui.setControlItemElements()](/XMLUI_object/xmlui8.md) | Sets the label, value pairs of the current item.                                            |
| [xmlui.setEnabled()](/XMLUI_object/xmlui9.md)             | Enables or disables (dims) a control.                                                       |
| [xmlui.setVisible()](/XMLUI_object/xmlui10.md)             | Shows or hides a control.                                                                   |

<span id="xmlui.accept()" class="anchor"></span>



## C-LevelExtensibility

#### About extensibility

This chapter describes the C-level extensibility mechanism, which lets you implement Adobe Animate extensibility files using a combination of JavaScript and custom C code.

***Note:** Adobe Animate runs on 64-bit operating systems only. All C extensions for this release must be built (or rebuilt) for 64 bit support.*

To implement extensibility, you define functions using C, bundle them in a dynamic linked library (DLL) or a shared library, save the library in the appropriate directory, and then call the functions from JavaScript using the Adobe Animate JavaScript API.
For example, you might want to define a function that performs intense calculations more efficiently than JavaScript does, which improves performance, or when you want to create more advanced tools or effects.
This extensibility mechanism is a subset of the Adobe Dreamweaver API. If you are familiar with that API, you might recognize the functions in the C-level extensibility mechanism API. However, this API differs from the Dreamweaver API in the following ways:

-   This API does not contain all the commands in the Dreamweaver API.

-   All declarations of type *wchar_t* and char in the Dreamweaver API are implemented as unsigned short declarations in this API, to support Unicode when strings are passed.

-   The [JSVal JS_BytesToValue()](/C-Level_Extensibility/The_C.md) function in this API is not part of the Dreamweaver API.

-   The location in which the DLL or shared library files must be stored is different (see ["Integrating C functions"](/C-Level_Extensibility/Integrating_C_functions.md)).

<span id="Integrating_C_functions" class="anchor"></span>



[IntegratingCfunctions](./C-Level_Extensibility/Integrating_C_functions.md)

[Datatypes](./C-Level_Extensibility/Data_types.md)

[TheC-levelAPI](./C-Level_Extensibility/The_C.md)
