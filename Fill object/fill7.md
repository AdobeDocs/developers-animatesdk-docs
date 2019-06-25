## fill.overflow

#### Availability

> Flash 8.

#### Usage

> fill.overflow

#### Description

> Property; a string that specifies the behavior of a gradient’s overflow. Acceptable values are "extend", "repeat", and
>
> "reflect"; the strings are not case-sensitive. The default value is "extend".

#### Example

> The following example specifies that the behavior of the overflow for the current selection should be "extend":
>
> var fill = fl.getDocumentDOM().getCustomFill(); fill.overflow = "extend"; fl.getDocumentDOM().setCustomFill(fill);
