## FLfile.setAttributes()

#### Availability

Flash MX 2004 7.2.

#### Usage

FLfile.setAttributes(fileURI, strAttrs)

#### Parameters

**fileURI** A string, expressed as a file:/// URI, specifying the file whose attributes you want to set.
**strAttrs** A string specifying values for the attribute(s) you want to set. For acceptable values for *strAttrs*, see the "Description" section below.

#### Returns

A Boolean value of true if successful.
***Note:** Results are unpredictable if the file or folder doesn’t exist. You should use* *[FLfile.exists()](#_bookmark563) before using this method.*

#### Description

Method; specifies system-level attributes for the specified file.
The following values are valid for *strAttrs*:

-   N — No specific attributes (not read-only, not hidden, and so on)

-   A — Ready for archiving (Windows only)

-   R — Read-only (on the Macintosh, read-only means "locked")

-   W — Writable (overrides R)

-   H — Hidden (Windows only)

-   V — Visible (overrides H, Windows only)

If you include both R and W in *strAttrs*, the R is ignored and the file is set as writable. Similarly, if you pass H and V, the
H is ignored and the file is set as visible.
If you want to make sure the archive attribute is not set, use this command with the N parameter before setting attributes. That is, there is no direct counterpart to A that turns off the archive attribute.

#### Examples

```
The following example sets the file mydata.txt to be read-only and hidden. It has no effect on the archive attribute.
var URI = "file:///c\|/temp/mydata.txt"; if (FLfile.exists(URI)) {
FLfile.setAttributes(URI, "RH");
}
The following example sets the file mydata.txt to be read-only and hidden. It also ensures that the archive attribute is not set.
var URI = "file:///c\|/temp/mydata.txt";
if (FLfile.exists(URI)) { FLfile.setAttributes(URI, "N"); FLfile.setAttributes(URI, "RH");
}

```
#### See also

[FLfile.getAttributes()](#_bookmark564)
