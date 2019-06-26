## fill.style

#### Availability

> Flash MX 2004. Value "bitmap" added in Flash CS4 Professional.

#### Usage

> fill.style

#### Description

> Property; a string that specifies the fill style. Acceptable values are "bitmap", "solid", "linearGradient", "radialGradient", and "noFill".
>
> If this value is "linearGradient" or "radialGradient", the [fill.colorArray](#_bookmark417) and [fill.posArray](#_bookmark422) properties are also available. If this value is "bitmap", the [fill.bitmapIsClipped](#_bookmark414) and [fill.bitmapPath](#_bookmark415) properties are also available.

#### Example

> The following example specifies the colors to use in a linear gradient for the current selection:
>
> var fill = fl.getDocumentDOM().getCustomFill(); fill.style= "linearGradient";
>
> fill.colorArray = \[ 0x00ff00, 0xff0000, 0x0000ff \]; fill.posArray= \[0,100, 200\]; fl.getDocumentDOM().setCustomFill( fill );
