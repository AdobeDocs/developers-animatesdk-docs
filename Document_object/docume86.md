## document.getTelemetryForSwf()

#### Availability

Adobe Animate.

#### Usage

document.getTelemetryForSwf( )

#### Parameters

None.

#### Returns

Returns boolean. Returns true if the "Enable detailed telemetry" checkbox is selected; otherwise false.

#### Description

Method; Indicates whether if the "Enable detailed telemetry" checkbox is selected in the Publish Settings dialog.

#### Example


The following example calls getTelemetryFromSwf():
```javascript
fl.trace("is detailed telemetry enabled for this doc: " + fl.getDocumentDOM().getTelemetryForSwf());

```