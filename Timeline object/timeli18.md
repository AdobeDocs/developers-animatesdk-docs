## timeline.expandFolder()

#### Availability

> Flash MX 2004.

#### Usage

> timeline.expandFolder(bExpand \[, bRecurseNestedParents \[, index\]\])

#### Parameters

> **bExpand** A Boolean value that, if set to true, causes the method to expand the folder; false causes the method to collapse the folder.
>
> **bRecurseNestedParents** A Boolean value that, if set to true, causes all the layers within the specified folder to be opened or closed, based on the *bExpand* parameter. This parameter is optional.
>
> **index** A zero-based index of the folder to expand or collapse. Use -1 to apply to all layers (you also must set *bRecurseNestedParents* to true). This property is equivalent to the Expand All/Collapse All menu items in the Flash authoring tool. This parameter is optional.

#### Returns

> Nothing.

#### Description

> Method; expands or collapses the specified folder or folders. If you do not specify a layer, this method operates on the current layer.

#### Example

> The following examples use this folder structure:
>
> Folder 1 \*\*\*
>
> --layer 7
>
> --Folder 2 \*\*\*\*
>
> ----Layer 5
>
> The following example expands Folder 1 only:
>
> fl.getDocumentDOM().getTimeline().currentLayer = 1; fl.getDocumentDOM().getTimeline().expandFolder(true);
>
> The following example expands Folder 1 only (assuming that Folder 2 collapsed when Folder 1 last collapsed; otherwise, Folder 2 appears expanded):
>
> fl.getDocumentDOM().getTimeline().expandFolder(true, false, 0); The following example collapses all folders in the current timeline: fl.getDocumentDOM().getTimeline().expandFolder(false, true, -1);
