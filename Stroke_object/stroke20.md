## stroke.style

#### Availability

Flash MX 2004.

#### Usage

stroke.style

#### Description

Property; a string that describes the stroke style. Acceptable values are "noStroke","solid", "dashed", "dotted", "ragged", "stipple", and "hatched". Some of these values require additional properties of the Stroke object to be set, as described in the following list:

-   If value is "solid" or "noStroke", there are no other properties.

-   If value is "dashed", there are two additional properties: dash1 and dash2.

-   If value is "dotted", there is one additional property: dotSpace.

-   If value is "ragged", there are three additional properties: pattern, waveHeight, and waveLength.

-   If value is "stipple", there are three additional properties: dotSize, variation, and density.

-   If value is "hatched", there are six additional properties: hatchThickness, space, jiggle, rotate, curve, and

length.

#### Example

```javascript
The following example sets the stroke style to ragged:
var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.style = "ragged"; fl.getDocumentDOM().setCustomStroke(myStroke);

```