## symbolInstance.cacheAsBitmap

#### Availability

Flash 8.

#### Usage

symbolInstance.cacheAsBitmap

#### Description

Property; a Boolean value that specifies whether run-time bitmap caching is enabled.
>
***Note:** Starting w/ Flash Professional CS5.5, users should switch to using the [“symbolInstance.bitmapRenderMode”](#_bookmark920)* *[on page 470](#_bookmark920) property instead of this property.*

#### Example

```
The following example enables run-time bitmap caching for the first element in the first frame on the first layer:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].cacheAsBitmap = true;

```