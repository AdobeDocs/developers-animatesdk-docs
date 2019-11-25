## componentInstance.parameters

#### Availability

Flash MX 2004.

#### Usage

*componentInstance.parameters*

#### Description

Read-only property; an array of ActionScript 2.0 properties that are accessible from the component Property inspector. See [Parameter object](../Parameter_object/parameter_summary.md).

#### Example

```javascript
The following example illustrates getting and setting the parameters property:
var parms = fl.getDocumentDOM().selection[0].parameters; parms[0].value = "some value";

```
#### See also

[Parameter object](../Parameter_object/parameter_summary.md)
