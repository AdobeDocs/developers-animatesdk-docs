## stroke.pattern

#### Availability

> Flash MX 2004.

#### Usage

> stroke.pattern

#### Description

> Property; a string that specifies the pattern of a ragged line. This property is available only if the stroke.style property is set to ragged (see [stroke.style](#_bookmark898)). Acceptable values are "solid", "simple", "random", "dotted", "random dotted", "triple dotted", and "random triple dotted".

#### Example

> The following example sets the pattern property to random for a stroke style of ragged:
>
> var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.style = "ragged";
>
> myStroke.pattern = "random"; fl.getDocumentDOM().setCustomStroke(myStroke);
