## text.lineType

#### Availability

Flash MX 2004.

#### Usage

text.lineType

#### Description

Property; a string that sets the line type. Acceptable values are "single line", "multiline", "multiline no wrap", and "password".
>
This property works only with dynamic or input text and generates a warning if used with static text. The "password"
>
value works only for input text.

#### Example

```
The following example sets the lineType property to the value multiline no wrap: fl.getDocumentDOM().selection\[0\].lineType = "multiline no wrap";

```