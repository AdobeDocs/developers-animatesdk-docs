## timeline.insertFrames()

#### Availability

> Flash MX 2004.

#### Usage

> timeline.insertFrames(\[numFrames \[, bAllLayers \[, frameNumIndex\]\]\])

#### Parameters

> **numFrames** An integer that specifies the number of frames to insert. If you omit this parameter, the method inserts frames at the current selection in the current layer. This parameter is optional.
>
> **bAllLayers** A Boolean value that, if set to true, causes the method to insert the specified number of frames in the *numFrames* parameter into all layers; if set to false (the default), the method inserts frames into the current layer. This parameter is optional.
>
> **frameNumIndex** A zero-based index that specifies the frame at which to insert a new frame. This parameter is optional.

#### Returns

> Nothing.

#### Description

> Method; inserts the specified number of frames at the specified index. If no parameters are specified, this method works as follows:

-   If one or more frames are selected, the method inserts the selected number of frames at the location of the first selected frame in the current layer. That is, if frames 6 through 10 are selected (a total of five frames), the method adds five frames at Frame 6 in the layer containing the selected frames.

-   If no frames are selected, the method inserts one frame at the current frame on all layers. If parameters are specified, the method works as follows:

-   If only *numFrames* is specified, inserts the specified number of frames at the current frame on the current layer.

-   If *numFrames* is specified and *bAllLayers* is true, inserts the specified number of frames at the current frame on all layers.

-   If all three parameters are specified, inserts the specified number of frames at the specified index (*frameIndex*); the value passed for *bAllLayers* determines if the frames are added only to the current layer or to all layers.

> If the specified or selected frame is a regular frame, the frame is inserted at that frame. For example, if you have a span of 10 frames numbered 1-10 and you select Frame 5 (or pass a value of 4 for *frameIndex*), this method adds a frame at Frame 5, and the length of the frame span becomes 11 frames. If Frame 5 is selected and it is a keyframe, this method inserts a frame at Frame 6 regardless of whether the frame next to it is also a keyframe.

#### Example

> The following example inserts a frame (or frames, depending on the selection) at the current selection in the current layer:
>
> fl.getDocumentDOM().getTimeline().insertFrames();
>
> The following example inserts five frames at the current frame in all layers:
>
> fl.getDocumentDOM().getTimeline().insertFrames(5);
>
> ***Note:** If you have multiple layers with frames in them, and you select a frame in one layer when using the previous command, Flash inserts the frames in the selected layer only. If you have multiple layers with no frames selected in them, Flash inserts the frames in all layers.*
>
> The following example inserts three frames in the current layer only:
>
> fl.getDocumentDOM().getTimeline().insertFrames(3, false);
>
> The following example inserts four frames in all layers, starting from the first frame:
>
> fl.getDocumentDOM().getTimeline().insertFrames(4, true, 0);
