## <img src="/media/image1.png" style="width:0.25005in;height:0.25005in" />document.exportVideo()

#### Availability

Adobe Animate.

#### Usage

exportVideo( fileURI \[, convertInAdobeMediaEncoder\] \[, transparent\] \[, stopAtFrame\] \[, stopAtFrameOrTime\] )

#### Parameters

**fileURI** A string, expressed as a file:/// URI, that specifies the fully qualified path to which the video is saved.
**convertInAdobeMediaEncoder** A boolen value that specifies whether or not to send the recorded video to Adobe Media Encoder. The default value is true, which sends the video to Adobe Media Encoder. This parameter is optional.
**transparent** A boolean value that specifies whether or not the background should be included in the video. The default value is false, which includes the movie background in the video. This parameter is optional.
**stopAtFrame** A boolean value that specifies whether the video should be recorded until it reaches a certain frame or a specific time. The default value is true, stop when a certain frame is reached. This parameter is optional.
**stopAtFrameOrTime** If stopAtFrame is true, this is an int specifying the number of frames to record. If stopAtFrame is false, this is the number of milliseconds to record. The default value is 0 which, if stopAtFrame is true, will record all the frames in the main timeline. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; exports a video from the document and optionally sends it to Adobe Media Encoder to convert the video.

#### Example

```
The following example illustrates the use of this method:
fl.getDocumentDOM().exportVideo("file:///C\|/myProject/myVideo.mov");

```