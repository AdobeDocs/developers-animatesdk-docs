## What’s new in the JavaScript API

The following section lists new objects, methods, and properties in Flash CC. It also lists changes in Flash CS5, CS5.5, and CS6.
>
If you have not used the JavaScript API before, you might want to skip this section and go directly to [“JavaScript API](#JavaScript_API_objects) [objects” on page 10](#JavaScript_API_objects)).

### New methods and properties in Flash CC

The following methods and properties for existing objects are new in Flash Profesional CC:

-   [Tween Object](#_bookmark1123)

    -   Tween.getColorTransform( )

    -   Tween.getFilters( )

    -   Tween.getGeometricTransform()

    -   Tween.getShape( )

    -   Tween.duration

    -   Tween.startFrame

    -   Tween.tweenType

-   [CompiledClipInstance object](#_bookmark67)

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

-   [Document object](#_bookmark116)

    -   Document.convertSelectionToBitmap()

    -   Document.distributeToKeyframes()

    -   Document.exportVideo()

    -   Document.getPublishDocumentData()

    -   Document.getTelemetryForSwf()

    -   Document.importFile() showDialog and showImporterUI properties

    -   Document.setPublishDocumenData()

-   [Element object](#_bookmark374)

    -   Element.getPublishPersistentData()

    -   Element.setPublishPersistentData()

-   [flash object (fl)](#_bookmark447)

    -   Flash.addEventListener()prePublish, postPublish, selectionChanged, and dpiChanged events

    -   fl.getThemeColor()

    -   fl.getThemeColorParameters()

    -   fl.getThemeFontInfo()

    -   fl.setPrefBoolean()

    -   fl.toggleBreakPoint()

    -   fl.xmlPanel()

    -   fl.xmlPanelFromString()

-   [Frame object](#_bookmark595)

    -   Frame.convertToFrameByFrameAnimation()

    -   Frame.getSoundEnvelope()

    -   Frame.getSoundEnvelopeLimits()

    -   Frame.setSoundEnvelope()

    -   Frame.setSoundEnvelopeLimits()

    -   Frame.isEmpty()

-   [Item object](#_bookmark658)

    -   item.getPublishData()

    -   item.setPublishData()

-   [library object](#_bookmark693)

    -   library.unusedItems

-   [swfPanel object](#_bookmark904)

    -   swfPanel.dpiScaleFactorX

    -   swfPanel.dpiScaleFactorY

    -   swfPanel.reload()

-   [SymbolInstance object](#_bookmark914)

    -   SymbolInstance.brightness

    -   SymbolInstance.tintColor

    -   SymbolInstance.tintPercent

-   [Timeline object](#_bookmark1030)

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

-   [SpriteSheetExporter object](#_bookmark844)

### New methods and properties in Flash CS6

The following methods and properties for existing objects are new in Flash Pro CS6:

-   [BitmapItem object](#_bookmark49)

    -   bitmapItem.exportToFile()quality parameter

    -   bitmapItem.hasValidAlphaLayer

    -   bitmapItem.lastModifiedDate

-   [Document object](#_bookmark116)

    -   document.exportInstanceToLibrary()

    -   document.exportInstanceToPNGSequence()

    -   document.getSWFPathFromProfile()

    -   document.saveAsCopy()

    -   document.swfJPEGQuality

-   [flash object (fl)](#_bookmark447)

    -   fl.spriteSheetExporter

-   [Layer object](#_bookmark679)

    -   layer.animationType

-   [Math object](#_bookmark718)

    -   Math.transformPoint()

-   [Shape object](#_bookmark805)

    -   shape.isFloating

-   [SoundItem object](#_bookmark827)

    -   soundItem.lastModifiedDate

-   [SymbolInstance object](#_bookmark914)

    -   symbolInstance.is3D

-   [SymbolItem object](#_bookmark950)

    -   symbolItem.exportToLibrary()

    -   symbolItem.exportToPNGSequence()

    -   symbolItem.lastModifiedDate

-   [Text object](#_bookmark967)

    -   text.filters

-   [VideoItem object](#_bookmark1140)

    -   videoItem.lastModifiedDate

### New methods and properties in Flash CS5 and CS5.5

The following methods and properties for existing objects are new in Flash Pro CS5:

-   [Document object](#_bookmark116)

    -   document.debugMovie()

    -   document.loadCuepointXML()

-   [flash object (fl)](#_bookmark447)

    -   fl.languageCode

    -   fl.toggleBreakpoint

-   [Frame object](#_bookmark595)

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

-   [Timeline object](#_bookmark1030)

    -   timeline.createMotionObject()

    -   timeline.libraryItem

    -   timeline.removeMotionObject()

    -   timeline.startPlayback

    -   timeline.stopPlayback

The following methods and properties for existing objects are new in Flash Pro CS5.5:

-   [SymbolInstance object](#_bookmark914)

    -   symbolInstance.bitmapRenderMode

    -   symbolInstance.backgroundColor

    -   symbolInstance.usesBackgroundColor

    -   symbolInstance.visible

-   [Timeline object](#_bookmark1030)

    -   timeline.copyLayers()

    -   timeline.cutLayers()

    -   timeline.duplicateLayers()

    -   timeline.pasteLayers()

-   [flash object (fl)](#_bookmark447)

    -   fl.getSwfPanel()

    -   fl.installedPlayers()

    -   fl.publishCacheEnabled

    -   fl.publishCacheDiskSizeMax

    -   fl.publishCacheMemorySizeMax

    -   fl.publishCacheMemoryEntrySizeLimit

    -   fl.clearPublishCache()

-   [swfPanel object](#_bookmark904)

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

<span id="JavaScript_API_objects" class="anchor"></span>

