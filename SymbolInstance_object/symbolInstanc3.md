## symbolInstance.bitmapRenderMode

#### Availability

Flash CS5.5 Professional.

#### Usage

symbolInstance.bitmapRenderMode

#### Description

Property; a string that sets the display type for the symbol. Acceptable values include:

-   "none"

-   "cache" - sets the symbol to be cached as a bitmap by Flash Player at runtime.

-   "export" - sets the symbol to be exported as a bitmap when the SWF is compiled.

The older ["symbolInstance.cacheAsBitmap" on page 472](#_bookmark925) property is similar to this property, but it offers fewer choices since it's a boolean. In the future, the cacheAsBitmap property may be deprecated, so users should switch to this new property. The true/false options in the boolean cacheAsBitmap property are the same as the "cache" / "none" values for this new property.

#### Example

```
The following example assigns the symbol’s bitmapRenderMode to "export":
var symbol = fl.getDocumentDOM().selection\[0\]; fl.trace(symbol.bitmapRenderMode); symbol.bitmapRenderMode = "export";

```