## timeline.setSelectedLayers()

#### Availability

Flash MX 2004.

#### Usage

timeline.setSelectedLayers(index \[, bReplaceCurrentSelection\])

#### Parameters

**index** A zero-based index for the layer to select.
**bReplaceCurrentSelection** A Boolean value that, if it is set to true, causes the method to replace the current selection; false causes the method to extend the current selection. The default value is true. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; sets the layer to be selected, and also makes the specified layer the current layer. Selecting a layer also means that all the frames in the layer are selected.

#### Example

```javascript
The following example selects the top layer: fl.getDocumentDOM().getTimeline().setSelectedLayers(0); The following example adds the next layer to the selection:
fl.getDocumentDOM().getTimeline().setSelectedLayers(1, false);

```
#### See also

[timeline.getSelectedLayers()](../Timeline_object/timeli26.md)
