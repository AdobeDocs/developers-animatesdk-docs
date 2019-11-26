## document.debugMovie()

#### Availability

Flash Professional CS5.

#### Usage

document.DebugMovie([Boolean abortIfErrorsExist])

#### Description

Method; Invokes the Debug Movie command on the document.

#### Parameters

**abortIfErrorsExist** Boolean; the default value is false. If set to true, the debug session will not start and the .swf window will not open if there are compiler errors. Compiler warnings will not abort the command.

#### Example

```javascript
The following example opens the current document in debug mode, but aborts the operation if compiler errors exist:
fl.getDocumentDOM().debugMovie(1);

```