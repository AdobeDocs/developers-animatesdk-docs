## compiledClipInstance.cacheAsBitmap

#### Availability

Adobe Animate.

#### Usage

compiledClipInstance.cacheAsBitmap

#### Description

Property; a boolean that indicates whether to cache bitmaps. (Equivalent to Use runtime bitmap caching in the Property Inspector). The default is false.

#### Example

```javascript
The following example illustrates use of this property:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].cacheAsBitmap = true;

```