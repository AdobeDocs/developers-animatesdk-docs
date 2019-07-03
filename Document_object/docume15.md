## document.arrange()

#### Availability

Flash MX 2004.

#### Usage

document.arrange(arrangeMode)

#### Parameters

**arrangeMode** Specifies the direction in which to move the selection. Acceptable values are "back", "backward", "forward", and "front". It provides the same capabilities as these options provide on the Modify \Arrange menu.

#### Returns

Nothing.

#### Description

Method; arranges the selection on the Stage. This method applies only to non-shape objects.

#### Example

```
The following example moves the current selection to the front:
fl.getDocumentDOM().arrange("front");

```