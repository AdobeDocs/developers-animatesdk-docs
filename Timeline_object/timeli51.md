## timeline.mergeLayers()

#### Availability

Adobe Animate 2020.

#### Usage

timeline.mergeLayers(startLayerNum:int,endLayerNum:int).

#### Parameters
startLayerNum:int:0

endLayerNum:int:0

#### Returns

Nothing.

#### Description

Method; Merge the layer at a specified index, or a range of layers

#### Example

The following example merge layers from index 0 to 3.
```javascript
fl.getDocumentDOM().getTimeline().mergeLayers(0,3)
```