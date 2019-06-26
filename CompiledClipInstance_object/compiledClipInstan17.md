## compiledClipInstance.forceSimple

#### Availability

> Flash MX 2004.

#### Usage

> compiledClipInstance.forceSimple

#### Description

> Property; a Boolean value that enables and disables the children of the object to be accessible. This is equivalent to the inverse logic of the Make Child Objects Accessible setting in the Accessibility panel. If forceSimple is true, it is the same as the Make Child Objects Accessible option being unchecked. If forceSimple is false, it is the same as the Make Child Object Accessible option being checked.

#### Example

> The following example illustrates getting and setting the forceSimple property:
>
> // Query if the children of the object are accessible.
>
> var areChildrenAccessible = fl.getDocumentDOM().selection\[0\].forceSimple;
>
> // Allow the children of the object to be accessible. fl.getDocumentDOM().selection\[0\].forceSimple = false;
