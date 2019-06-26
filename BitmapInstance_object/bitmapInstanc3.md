## bitmapInstance.vPixels

#### Availability

> Flash MX 2004.

#### Usage

> bitmapInstance.vPixels

#### Description

> Read-only property; an integer that represents the height of the bitmap—that is, the number of pixels in the vertical dimension.

#### Example

> The following code gets the height of the bitmap in pixels:
>
> // Get the number of pixels in the vertical dimension. var bmObj = fl.getDocumentDOM().selection\[0\];
>
> var isBitmap = bmObj.instanceType; if(isBitmap == "bitmap"){
>
> var numVerticalPixels = bmObj.vPixels;
>
> }

#### See also

> [bitmapInstance.hPixels](#_bookmark45)
