## document.punch()

#### Availability

> Flash 8.

#### Usage

> document.punch()

#### Parameters

> None.

#### Returns

> None.

#### Description

> Method; uses the top selected drawing object to punch through all selected drawing objects underneath it. If no objects are selected, calling this method results in an error and the script breaks at that point.

#### Example

> The following example punches through drawing objects underneath the selected drawing object:
>
> fl.getDocumentDOM().punch();

#### See also

> [document.crop()](#_bookmark159), [document.deleteEnvelope()](#_bookmark164), [document.intersect()](#_bookmark229), [document.union()](#_bookmark336), [shape.isDrawingObject](#_bookmark816)
