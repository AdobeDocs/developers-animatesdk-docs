## What’s new in the JavaScript API

The following section lists new objects, methods, and properties in Animate. It also lists changes in Flash CC, CS6, CS5.5, and CS5.
If you have not used the JavaScript API before, you might want to skip this section and go directly to [JavaScript API objects](#!../Introduction/JavaScript_API_objects.md).

### New methods and properties in Animate 2020
The following methods and properties for existing objects are new in Animate 2020:

-   [Document object](#!../Document_object/document_summary.md)

    -   document.getTaggedSwatches()

    -   document.getTaggedSwatchByName()

    -   document.getTaggedSwatchAtIndex()

    -   document.setTaggedSwatchByName()

    -   document.setTaggedSwatchAtIndex()

    -   document.addTaggedSwatch()

    -   document.addTaggedSwatchWithColor()

    -   document.deleteTaggedSwatchByName()

    -   document.deleteTaggedSwatchAtIndex()

    -   document.getTaggedSwatchesPaletteList()

    -   document.getIndexForTaggedSwatchesPalette()

    -   document.convertToDoc()

    -   document.exportCanvasPublishTemplate()

    -   document.importCanvasPublishTemplate()

    -   document.exportMedia()

    -   document.exportSVG()

-   [Layer object](#!../Layer_object/layer_summary.md)

    -   layer.getZDepthAtFrame()

    -   layer.setZDepthAtFrame()

    -   layer.getRigParentAtFrame()

    -   layer.setRigParentAtFrame()

    -   layer.getRigMatrixAtFrame()

    -   layer.getFiltersAtFrame()

    -   layer. setFiltersAtFrame()

    -   layer.getColorTransformAtFrame()

    -   layer.setColorTransformAtFrame()

    -   layer.getBlendModeAtFrame()

    -   layer.setBlendModeAtFrame()

-   [Timeline object](#!../Timeline_object/timeline_summary.md)

    -   timeline.advancedLayersEnabled

    -   timeline.mergeLayers()

-   [flash object (fl)](#!../flash_object_(fl)/fl_summary.md)

    -   fl.addToolInToolbar()


### New objects in Animate 2020
The following object is new in Flash CS6:

-   [TextureAtlasExporter object](#!../TextureAtlasExporter_object/TextureAtlasExporter_summary.md)

-   [Camera object](#!../Camera_object/Camera_summary.md)

### New methods and properties in Flash CC

The following methods and properties for existing objects are new in Flash Profesional CC:

-   [Tween Object](#!../Tween_Object/Tween_object_Summary.md)

    -   Tween.getColorTransform( )

    -   Tween.getFilters( )

    -   Tween.getGeometricTransform()

    -   Tween.getShape( )

    -   Tween.duration

    -   Tween.startFrame

    -   Tween.tweenType

-   [CompiledClipInstance object](#!../CompiledClipInstance_object/compiledClipInstance_summary.md)

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

-   [Document object](#!../Document_object/document_summary.md)

    -   Document.convertSelectionToBitmap()

    -   Document.distributeToKeyframes()

    -   Document.exportVideo()

    -   Document.getPublishDocumentData()

    -   Document.getTelemetryForSwf()

    -   Document.importFile() showDialog and showImporterUI properties

    -   Document.setPublishDocumenData()

-   [Element object](#!../Element_object/element_summary.md)

    -   Element.getPublishPersistentData()

    -   Element.setPublishPersistentData()

-   [flash object (fl)](#!../flash_object_(fl)/fl_summary.md)

    -   Flash.addEventListener()prePublish, postPublish, selectionChanged, and dpiChanged events

    -   fl.getThemeColor()

    -   fl.getThemeColorParameters()

    -   fl.getThemeFontInfo()

    -   fl.setPrefBoolean()

    -   fl.toggleBreakPoint()

    -   fl.xmlPanel()

    -   fl.xmlPanelFromString()

-   [Frame object](#!../Frame_object/frame_summary.md)

    -   Frame.convertToFrameByFrameAnimation()

    -   Frame.getSoundEnvelope()

    -   Frame.getSoundEnvelopeLimits()

    -   Frame.setSoundEnvelope()

    -   Frame.setSoundEnvelopeLimits()

    -   Frame.isEmpty()

-   [Item object](#!../Item_object/item_summary.md)

    -   item.getPublishData()

    -   item.setPublishData()

-   [library object](#!../library_object/library_summary.md)

    -   library.unusedItems

-   [swfPanel object](#!../swfPanel_object/swfPanel_summary.md)

    -   swfPanel.dpiScaleFactorX

    -   swfPanel.dpiScaleFactorY

    -   swfPanel.reload()

-   [SymbolInstance object](#!../SymbolInstance_object/symbolInstance_summary.md)

    -   SymbolInstance.brightness

    -   SymbolInstance.tintColor

    -   SymbolInstance.tintPercent

-   [Timeline object](#!../Timeline_object/timeline_summary.md)

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

-   [SpriteSheetExporter object](#!../SpriteSheetExporter_object/SpriteSheetExporter_summary.md)

### New methods and properties in Flash CS6

The following methods and properties for existing objects are new in Flash Pro CS6:

-   [BitmapItem object](#!../BitmapItem_object/bitmapItem_summary.md)

    -   bitmapItem.exportToFile()quality parameter

    -   bitmapItem.hasValidAlphaLayer

    -   bitmapItem.lastModifiedDate

-   [Document object](#!../Document_object/document_summary.md)

    -   document.exportInstanceToLibrary()

    -   document.exportInstanceToPNGSequence()

    -   document.getSWFPathFromProfile()

    -   document.saveAsCopy()

    -   document.swfJPEGQuality

-   [flash object (fl)](#!../flash_object_(fl)/fl_summary.md)

    -   fl.spriteSheetExporter

-   [Layer object](#!../Layer_object/layer_summary.md)

    -   layer.animationType

-   [Math object](#!../Math_object/Math_summary.md)

    -   Math.transformPoint()

-   [Shape object](#!../Shape_object/shape_summary.md)

    -   shape.isFloating

-   [SoundItem object](#!../SoundItem_object/soundItem_summary.md)

    -   soundItem.lastModifiedDate

-   [SymbolInstance object](#!../SymbolInstance_object/symbolInstance_summary.md)

    -   symbolInstance.is3D

-   [SymbolItem object](#!../SymbolItem_object/symbolItem_summary.md)

    -   symbolItem.exportToLibrary()

    -   symbolItem.exportToPNGSequence()

    -   symbolItem.lastModifiedDate

-   [Text object](#!../Text_object/text_summary.md)

    -   text.filters

-   [VideoItem object](#!../VideoItem_object/videoItem_summary.md)

    -   videoItem.lastModifiedDate

### New methods and properties in Flash CS5 and CS5.5

The following methods and properties for existing objects are new in Flash Pro CS5:

-   [Document object](#!../Document_object/document_summary.md)

    -   document.debugMovie()

    -   document.loadCuepointXML()

-   [flash object (fl)](#!../flash_object_(fl)/fl_summary.md)

    -   fl.languageCode

    -   fl.toggleBreakpoint

-   [Frame object](#!../Frame_object/frame_summary.md)

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

-   [Timeline object](#!../Timeline_object/timeline_summary.md)

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

-   [Timeline object](#../Timeline_object/timeline_summary.md)

    -   timeline.copyLayers()

    -   timeline.cutLayers()

    -   timeline.duplicateLayers()

    -   timeline.pasteLayers()

-   [flash object (fl)](#!../flash_object_(fl)/fl_summary.md)

    -   fl.getSwfPanel()

    -   fl.installedPlayers()

    -   fl.publishCacheEnabled

    -   fl.publishCacheDiskSizeMax

    -   fl.publishCacheMemorySizeMax

    -   fl.publishCacheMemoryEntrySizeLimit

    -   fl.clearPublishCache()

-   [swfPanel object](#!../swfPanel_object/swfPanel_summary.md)

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


