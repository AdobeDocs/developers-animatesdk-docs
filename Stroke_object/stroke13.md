## stroke.miterLimit

#### Availability

> Flash 8.

#### Usage

> stroke.miterLimit

#### Description

> Property; a float value that specifies the angle above which the tip of the miter will be truncated by a segment. That means the miter is truncated only if the miter angle is greater than the value of miterLimit.

#### Example

> The following example changes the miter limit of the stroke setting to 3. If the miter angle is greater than 3, the miter is truncated.
>
> var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.miterLimit = 3;
>
> var myStroke = fl.getDocumentDOM().setCustomStroke();
