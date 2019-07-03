## toolObj.showPIControl()

#### Availability

Flash MX 2004.

#### Usage

toolObj.showPIControl(control, bShow)

#### Parameters

**control** A string that specifies the name of the control to show or hide. This method is used only when you create extensible tools. Valid values depend on the Property inspector invoked by this tool (see [toolObj.setPI()](#_bookmark1098)).
A shape Property inspector has the following controls:

|        |      |
|--------|------|
| stroke | fill |

A text Property inspector has the following controls:

| type        | font         | pointsize   |
|-------------|--------------|-------------|
| color       | bold         | italic      |
| direction   | alignLeft    | alignCenter |
| alignRight  | alignJustify | spacing     |
| position    | autoKern     | small       |
| rotation    | format       | lineType    |
| selectable  | html         | border      |
| deviceFonts | varEdit      | options     |
| link        | maxChars     | target      |

The movie Property inspector has the following controls:

| size      | publish | background |
|-----------|---------|------------|
| framerate | player  | profile    |

**bShow** A Boolean value that determines whether to show or hide the specified control (true shows the control; false
hides the control).

#### Returns

Nothing.

#### Description

Method; shows or hides a control in the Property inspector. This method is used only when you create extensible tools.

#### Example

```
The following command in an extensible tool’s JavaScript file will set Flash to not show the fill options in the Property inspector for that tool:
fl.tools.activeTool.showPIControl("fill", false);

```