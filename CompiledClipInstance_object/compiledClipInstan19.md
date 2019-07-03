## compiledClipInstance.silent

#### Availability

Flash MX 2004.

#### Usage

compiledClipInstance.silent

#### Description

Property; a Boolean value that enables or disables the accessibility of the object; equivalent to the inverse logic of Make Object Accessible setting in the Accessibility panel. That is, if silent is true, then Make Object Accessible is unchecked. If silent is false, then Make Object Accessible is checked.

#### Example

```
The following example illustrates getting and setting the silent property:
// Query if the object is accessible.
var isSilent = fl.getDocumentDOM().selection\[0\].silent;
// Set the object to be accessible. fl.getDocumentDOM().selection\[0\].silent = false;

```