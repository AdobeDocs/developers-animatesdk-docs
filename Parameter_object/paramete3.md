## parameter.name

#### Availability

Flash MX 2004.

#### Usage

parameter.name

#### Description

Read-only property; a string that specifies the name of the parameter.

#### Example

```
The following example shows the name of the fifth parameter for the selected component:
var parms = fl.getDocumentDOM().selection\[0\].parameters; fl.trace("name: " + parms\[4\].name);
The following example shows the name of the fifth parameter for the specified screen:
var parms = fl.getDocumentDOM().screenOutline.screens\[1\].parameters; fl.trace("name: " + parms\[4\].name);

```