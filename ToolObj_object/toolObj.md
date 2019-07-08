## toolObj.depth

#### Availability

Flash MX 2004.

#### Usage

toolObj.depth

#### Description

Read-only property; an integer that specifies the depth of the tool in the pop-up menu in the Tools panel. This property is used only when creating extensible tools.

#### Example

```javascript
The following example specifies that the tool has a depth of 1, which means one level under a tool in the Tools panel:
fl.tools.activeTool.depth = 1;

```