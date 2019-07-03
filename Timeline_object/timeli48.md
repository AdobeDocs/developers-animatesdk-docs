## timeline.showLayerMasking()

#### Availability

Flash MX 2004.

#### Usage

timeline.showLayerMasking(\[layer\])

#### Parameters

**layer** A zero-based index of a mask or masked layer to show masking during authoring. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; shows the layer masking during authoring by locking the mask and masked layers. This method uses the current layer if no layer is specified. If you use this method on a layer that is not of type Mask or Masked, Flash displays an error in the Output panel.

#### Example

```
The following example specifies that the layer masking of the first layer should show during authoring.
fl.getDocumentDOM().getTimeline().showLayerMasking(0);

```