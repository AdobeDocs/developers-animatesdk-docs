## TextureAtlasExporter.app

#### Availability

Animate 2020.

#### Usage

TextureAtlasExporter.app

#### Description

Read-only property; A string indicating the name of the application that is generating the TextureAtlas. This property
is provided for use by any future TextureAtlas generator plugins that may be created for Animate 2020.

#### Example

``` javascript
var exporter = new TextureAtlasExporter;
alert(exporter.app);
// "Adobe Animate"
````