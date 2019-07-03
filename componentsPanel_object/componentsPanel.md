## componentsPanel.addItemToDocument()

#### Availability

Flash MX 2004.

#### Usage

componentsPanel.addItemToDocument(position, categoryName, componentName)

#### Parameters

**position** A point (for example, {x:0, y:100}) that specifies the location at which to add the component. Specify *position* relative to the center point of the component—not the component’s registration point (also *origin point* or *zero point*).
>
**categoryName** A string that specifies the name of the component category (for example, "Data"). The valid category names are listed in the Components panel.
>
**componentName** A string that specifies the name of the component in the specified category (for example, "WebServiceConnector"). The valid component names are listed in the Components panel.

#### Returns

Nothing.

#### Description

Adds the specified component to the document at the specified position.
>
**componentsPanel object**

#### Example

```
The following examples illustrate some ways to use this method:
fl.componentsPanel.addItemToDocument({x:0, y:0}, "User Interface", "CheckBox"); fl.componentsPanel.addItemToDocument({x:0, y:100}, "Data", "WebServiceConnector"); fl.componentsPanel.addItemToDocument({x:0, y:200}, "User Interface", "Button");

```