## symbolItem summary

> **Inheritance** [Item object](#_bookmark658) \> SymbolItem object

#### Availability

> Flash MX 2004.

#### Description

> The SymbolItem object is a subclass of the [Item object](#_bookmark658).

#### Method summary

> In addition to the Item object methods, you can use the following methods with the SymbolItem object:

| **Method**                                                                | **Description**                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [symbolItem.convertToCompiledClip()](#symbolItem.convertToCompiledClip()) | Converts a symbol item in the library to a compiled movie clip. |
| [symbolItem.exportSWC()](#_bookmark953)                                   | Exports the symbol item to a SWC file.                          |
| [symbolItem.exportSWF()](#_bookmark954)                                   | Exports the symbol item to a SWF file.                          |
| [symbolItem.exportToLibrary()](#_bookmark955)                             | Export an instance to a new bitmap in the Library.              |
| [symbolItem.exportToPNGSequence()](#_bookmark956)                         | Export a symbol to a sequence of PNG files.                     |

#### Property summary

> In addition to the Item object properties, the following properties are available for the SymbolItem object:

| **Property**                                  | **Description**                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------|
| [symbolItem.lastModifiedDate](#_bookmark957)  | A string hexadecimal value that indicates the modification date of the symbol.             |
| [symbolItem.scalingGrid](#_bookmark958)       | A Boolean value that specifies whether 9-slice scaling is enabled for the item.            |
| [symbolItem.scalingGridRect](#_bookmark959)   | A Rectangle object that specifies the locations of the four 9-slice guides.                |
| [symbolItem.sourceAutoUpdate](#_bookmark960)  | A Boolean value that specifies whether the item is updated when the FLA file is published. |
| [symbolItem.sourceFilePath](#_bookmark961)    | A string that specifies the path for the source FLA file as a file:/// URI.                |
| [symbolItem.sourceLibraryName](#_bookmark962) | A string that specifies the name of the item in the source file library.                   |
| [symbolItem.symbolType](#_bookmark963)        | A string that specifies the type of symbol.                                                |
| [symbolItem.timeline](#_bookmark964)          | Read-only; a [Timeline object](#_bookmark1030).                                            |

<span id="symbolItem.convertToCompiledClip()" class="anchor"></span>
