## symbolInstance.forceSimple

#### Availability

Flash MX 2004.

#### Usage

symbolInstance.forceSimple

#### Description

Property; a Boolean value that enables and disables the accessibility of the object’s children. This property is equivalent to the inverse logic of the Make Child Objects Accessible setting in the Accessibility panel. For example, if forceSimple is true, it is the same as the Make Child Object Accessible option being unchecked. If forceSimple is false, it is the same as the Make Child Object Accessible option being checked.
This property is available only for MovieClip objects.

#### Example

```
The following example checks to see if the children of the object are accessible; a return value of false means the children are accessible:
var areChildrenAccessible = fl.getDocumentDOM().selection\[0\].forceSimple; The following example allows the children of the object to be accessible: fl.getDocumentDOM().selection\[0\].forceSimple = false;

```