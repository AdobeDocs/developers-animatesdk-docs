## confirm()

#### Availability

Flash 8.

#### Usage

confirm ( strAlert )

#### Parameters

**strAlert** A string that specifies the message you want to display in the Alert dialog box.

#### Returns

A Boolean value: true if the user clicks OK; false if the user clicks Cancel.

#### Description

Method; displays a string in a modal Alert dialog box, along with OK and Cancel buttons.
***Note:** If there are no documents (FLA files) open, this method fails with an error condition.*

#### Example

```
The following example displays the message "Sort data?" in an Alert dialog box:
confirm("Sort data?");

```
#### See also

[alert()](#_bookmark16), [prompt()](#_bookmark28)
