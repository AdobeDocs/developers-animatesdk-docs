## document.as3AutoDeclare

#### Availability

Flash CS3 Professional.

#### Usage

document.as3AutoDeclare

#### Description

Property; a Boolean value that describes whether the instances placed on the Stage are automatically added to user- defined timeline classes. The default value is true.

#### Example

```javascript
The following example specifies that instances placed on the Stage in the current document must be manually added to user-defined timeline classes.
fl.getDocumentDOM().as3AutoDeclare=false;

```