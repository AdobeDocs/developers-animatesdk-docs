## toolObj.enablePIControl()

#### Availability

Flash MX 2004.

#### Usage

toolObj.enablePIControl(control, bEnable)

#### Parameters

**control** A string that specifies the name of the control to enable or disable. Legal values depend on the Property inspector invoked by this tool; see [toolObj.setPI()](../ToolObj_object/toolObj7.md).

A shape Property inspector has the following controls:
<table><thead></th></tr></thead><tbody><tr class="odd"><td>Stroke</td><td><p>fill</p></td></tr></tbody></table>

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

A movie Property inspector has the following controls:

<table><thead><tr class="header"><th>size</th><th>publish</th><th><p>background</p></th></tr></thead><tbody><tr class="odd"><td>framerate</td><td>player</td><td><p>profile</p></td></tr></tbody></table>

**bEnable** A Boolean value that determines whether to enable (true) or disable (false) the control.

#### Returns

Nothing.

#### Description

Method; enables or disables the specified control in a Property inspector. Used only when creating extensible tools.

#### Example

The following command in an extensible tool’s JavaScript file sets Flash to not show the stroke options in the Property inspector for that tool:

```javascript
theTool.enablePIControl("stroke",false); 


```