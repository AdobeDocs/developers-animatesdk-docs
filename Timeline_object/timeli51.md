## timeline.mergeLayers()

#### Availability

Animate 2020.

#### Usage

timeline.mergeLayers(startLayerNum:int,endLayerNum:int).

#### Parameters

**startLayerNum**:It is an integer that specifies the starting layer index.

**endLayerNum**:It is an integer that specifies the ending layer index.

#### Returns

Nothing.

#### Description

Method; Merge the layers within specified range of indexes.

#### Example

The following example merge layers from index 0 to 3.
```javascript
fl.getDocumentDOM().getTimeline().mergeLayers(0,3)
```