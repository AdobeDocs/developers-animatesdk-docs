## document.getBlendMode()

#### Availability

Flash 8.

#### Usage

document.getBlendMode()

#### Parameters

None.

#### Returns

A string that specifies the blending mode for the selected objects. If more than one object is selected and they have different blending modes, the string reflects the blending mode of the object with the highest depth.
***Note:** The return value is unpredictable if the selection contains objects that don’t support blending modes, or that have a blending mode value of "normal".*

#### Description

Method; returns a string that specifies the blending mode for the selected objects.

#### Example

```
The following example displays the name of the blending mode in the Output panel:
fl.trace(fl.getDocumentDom().getBlendMode());

```