## frame.setSoundEnvelopeLimits()

#### Availability

> Adobe Animate.

#### Usage

> frame.setSoundEnvelopeLimits(limits)

#### Parameters

> **limits** A structure that contains start and end fields that signify the limits for a custom sound envelope.

#### Returns

> Nothing.

#### Description

> Method; Sets the sound envelope limits of any frame with a sound file.

#### Example

> The following example illustrates the use of setSoundEnvelopeLimits:
>
> /var limits;
>
> limits.start = 2000; limits.end = 15000; fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].setSoundEnvelopeLimits(limits);

#### See also

> [frame.getSoundEnvelopeLimits()](#_bookmark608)
