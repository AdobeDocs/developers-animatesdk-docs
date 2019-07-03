## timeline.addMotionGuide()

#### Availability

Flash MX 2004.

#### Usage

timeline.addMotionGuide()

#### Parameters

None.

#### Returns

An integer that represents the zero-based index of the newly added guide layer. If the current layer type is not of type
"Normal", Flash returns -1.

#### Description

Method; adds a motion guide layer above the current layer and attaches the current layer to the newly added guide layer, converting the current layer to a layer of type "Guided".
This method functions only on a layer of type "Normal". It has no effect on a layer whose type is "Folder", "Mask", "Masked", "Guide", or "Guided".

#### Example

```
The following example adds a motion guide layer above the current layer, and converts the current layer to Guided: fl.getDocumentDOM().getTimeline().addMotionGuide();

```