# ImageMagick

[Official Site](http://www.imagemagick.org/)

[Thumbnail](http://www.imagemagick.org/Usage/thumbnails/)

### Usage
  1. Turn jpg to gif using thumbnail option<p>
  **convert** **-define** jpeg:size=500x180 *a.jpg* **-auto-orient** **-thumbnail** 250x90 -unsharp 0x.5 *b.gif*

  PS:<p>
  **-thumbnail**: This not only resizes the image, but strips any and all profile and comment information that may be present in the original JPEG image.<p>
  **-define jpeg:size=**: This is passed to the JPEG library, which will return an image somewhere between this size and double this size (if possible), rather that the whole very large original image. Basically don't overflow the computers memory with an huge image when it isn't needed.<p>
  **-auto-orient**: If the image from a digital camera is rotated correctly according to the camera's orientation. This is not needed for the 'desktop' image.<p>
  The **250** pixel width limit in the above is important. If left unset, ImageMagick would have complete width freedom (EG: using "-thumbnail x90" ). This could result in problems when generating thumbnails of long thin images.
