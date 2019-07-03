## fl.as3PackagePaths

#### Availability

Flash CS3 Professional.

#### Usage

fl.as3PackagePaths

#### Description

Property; a string that corresponds to the global Classpath setting in the ActionScript 3.0 Settings dialog box. Items in the string are delimited by semi-colons. To view or change ActionScript 2.0 Classpath settings, use [fl.packagePaths](#_bookmark512)
[- dropped](#_bookmark512).

#### Example

```
The following example illustrates changing the ActionScript 3.0 Classpath settings.
fl.trace(fl.as3PackagePaths);
// Output (assuming started with default value)
// .;$(AppConfig)/ActionScript 3.0/Classes fl.as3PackagePaths="buying;selling"; fl.trace(fl.as3PackagePaths);
// Output
// buying; selling

```
#### See also

[fl.resetAS3PackagePaths()](#_bookmark525)
