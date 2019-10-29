## What’s new in the JavaScript API

The following section lists new objects, methods, and properties in Animate. It also lists changes in Flash CC, CS6, CS5.5, and CS5.
If you have not used the JavaScript API before, you might want to skip this section and go directly to [JavaScript API objects](#JavaScript_API_objects).

### New methods and properties in Animate 2020
The following methods and properties for existing objects are new in Animate 2020:

-   [Document object](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/document_summary.md)

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

-   [Layer object](#!AdobeDocs/developers-animatesdk-docs/test/Layer_object/layer_summary.md)

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

-   [Timeline object](#!AdobeDocs/developers-animatesdk-docs/test/Timeline_object/timeline_summary.md)

    -   timeline.advancedLayersEnabled

    -   timeline.mergeLayers()

### New objects in Animate 2020
The following object is new in Flash CS6:

-   [TextureAtlasExporter object](#!AdobeDocs/developers-animatesdk-docs/test/TextureAtlasExporter_object/TextureAtlasExporter_summary.md)

-   [Camera object](#!AdobeDocs/developers-animatesdk-docs/test/Camera_object/Camera_summary.md)

### New methods and properties in Flash CC

The following methods and properties for existing objects are new in Flash Profesional CC:

-   [Tween Object](#!AdobeDocs/developers-animatesdk-docs/test/Tween_Object/Tween_object_Summary.md)

    -   Tween.getColorTransform( )

    -   Tween.getFilters( )

    -   Tween.getGeometricTransform()

    -   Tween.getShape( )

    -   Tween.duration

    -   Tween.startFrame

    -   Tween.tweenType

-   [CompiledClipInstance object](#!AdobeDocs/developers-animatesdk-docs/test/CompiledClipInstance_object/compiledClipInstance_summary.md)

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

-   [Document object](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/document_summary.md)

    -   Document.convertSelectionToBitmap()

    -   Document.distributeToKeyframes()

    -   Document.exportVideo()

    -   Document.getPublishDocumentData()

    -   Document.getTelemetryForSwf()

    -   Document.importFile() showDialog and showImporterUI properties

    -   Document.setPublishDocumenData()

-   [Element object](#!AdobeDocs/developers-animatesdk-docs/test/Element_object/element_summary.md)

    -   Element.getPublishPersistentData()

    -   Element.setPublishPersistentData()

-   [flash object (fl)](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl_summary.md)

    -   Flash.addEventListener()prePublish, postPublish, selectionChanged, and dpiChanged events

    -   fl.getThemeColor()

    -   fl.getThemeColorParameters()

    -   fl.getThemeFontInfo()

    -   fl.setPrefBoolean()

    -   fl.toggleBreakPoint()

    -   fl.xmlPanel()

    -   fl.xmlPanelFromString()

-   [Frame object](#!AdobeDocs/developers-animatesdk-docs/test/Frame_object/frame_summary.md)

    -   Frame.convertToFrameByFrameAnimation()

    -   Frame.getSoundEnvelope()

    -   Frame.getSoundEnvelopeLimits()

    -   Frame.setSoundEnvelope()

    -   Frame.setSoundEnvelopeLimits()

    -   Frame.isEmpty()

-   [Item object](#!AdobeDocs/developers-animatesdk-docs/test/Item_object/item_summary.md)

    -   item.getPublishData()

    -   item.setPublishData()

-   [library object](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library_summary.md)

    -   library.unusedItems

-   [swfPanel object](#!AdobeDocs/developers-animatesdk-docs/test/swfPanel_object/swfPanel_summary.md)

    -   swfPanel.dpiScaleFactorX

    -   swfPanel.dpiScaleFactorY

    -   swfPanel.reload()

-   [SymbolInstance object](#!AdobeDocs/developers-animatesdk-docs/test/SymbolInstance_object/symbolInstance_summary.md)

    -   SymbolInstance.brightness

    -   SymbolInstance.tintColor

    -   SymbolInstance.tintPercent

-   [Timeline object](#!AdobeDocs/developers-animatesdk-docs/test/Timeline_object/timeline_summary.md)

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

-   [SpriteSheetExporter object](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporter_summary.md)

### New methods and properties in Flash CS6

The following methods and properties for existing objects are new in Flash Pro CS6:

-   [BitmapItem object](#!AdobeDocs/developers-animatesdk-docs/test/BitmapItem_object/bitmapItem_summary.md)

    -   bitmapItem.exportToFile()quality parameter

    -   bitmapItem.hasValidAlphaLayer

    -   bitmapItem.lastModifiedDate

-   [Document object](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/document_summary.md)

    -   document.exportInstanceToLibrary()

    -   document.exportInstanceToPNGSequence()

    -   document.getSWFPathFromProfile()

    -   document.saveAsCopy()

    -   document.swfJPEGQuality

-   [flash object (fl)](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl_summary.md)

    -   fl.spriteSheetExporter

-   [Layer object](#!AdobeDocs/developers-animatesdk-docs/test/Layer_object/layer_summary.md)

    -   layer.animationType

-   [Math object](#!AdobeDocs/developers-animatesdk-docs/test/Math_object/Math_summary.md)

    -   Math.transformPoint()

-   [Shape object](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape_summary.md)

    -   shape.isFloating

-   [SoundItem object](#!AdobeDocs/developers-animatesdk-docs/test/SoundItem_object/soundItem_summary.md)

    -   soundItem.lastModifiedDate

-   [SymbolInstance object](#!AdobeDocs/developers-animatesdk-docs/test/SymbolInstance_object/symbolInstance_summary.md)

    -   symbolInstance.is3D

-   [SymbolItem object](#!AdobeDocs/developers-animatesdk-docs/test/SymbolItem_object/symbolItem_summary.md)

    -   symbolItem.exportToLibrary()

    -   symbolItem.exportToPNGSequence()

    -   symbolItem.lastModifiedDate

-   [Text object](#!AdobeDocs/developers-animatesdk-docs/test/Text_object/text_summary.md)

    -   text.filters

-   [VideoItem object](#!AdobeDocs/developers-animatesdk-docs/test/VideoItem_object/videoItem_summary.md)

    -   videoItem.lastModifiedDate

### New methods and properties in Flash CS5 and CS5.5

The following methods and properties for existing objects are new in Flash Pro CS5:

-   [Document object](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/document_summary.md)

    -   document.debugMovie()

    -   document.loadCuepointXML()

-   [flash object (fl)](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl_summary.md)

    -   fl.languageCode

    -   fl.toggleBreakpoint

-   [Frame object](#!AdobeDocs/developers-animatesdk-docs/test/Frame_object/frame_summary.md)

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

-   [Timeline object](#!AdobeDocs/developers-animatesdk-docs/test/Timeline_object/timeline_summary.md)

    -   timeline.createMotionObject()

    -   timeline.libraryItem

    -   timeline.removeMotionObject()

    -   timeline.startPlayback

    -   timeline.stopPlayback

The following methods and properties for existing objects are new in Flash Pro CS5.5:

-   [SymbolInstance object](#!AdobeDocs/developers-animatesdk-docs/test/SymbolInstance_object/symbolInstance_summary.md)

    -   symbolInstance.bitmapRenderMode

    -   symbolInstance.backgroundColor

    -   symbolInstance.usesBackgroundColor

    -   symbolInstance.visible

-   [Timeline object](#!AdobeDocs/developers-animatesdk-docs/test/Timeline_object/timeline_summary.md)

    -   timeline.copyLayers()

    -   timeline.cutLayers()

    -   timeline.duplicateLayers()

    -   timeline.pasteLayers()

-   [flash object (fl)](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl_summary.md)

    -   fl.getSwfPanel()

    -   fl.installedPlayers()

    -   fl.publishCacheEnabled

    -   fl.publishCacheDiskSizeMax

    -   fl.publishCacheMemorySizeMax

    -   fl.publishCacheMemoryEntrySizeLimit

    -   fl.clearPublishCache()

-   [swfPanel object](#!AdobeDocs/developers-animatesdk-docs/test/swfPanel_object/swfPanel_summary.md)

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


