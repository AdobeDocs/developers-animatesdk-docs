## document.currentTimeline

#### Availability

Flash MX 2004.

#### Usage

document.currentTimeline

#### Description

Property; an integer that specifies the index of the active timeline. You can set the active timeline by changing the value of this property; the effect is almost equivalent to calling [document.editScene()](../Document_object/docume57.md). The only difference is that you don’t get an error message if the index of the timeline is not valid; the property is simply not set, which causes silent failure.

#### Example

```javascript
The following example displays the index of the current timeline:

var myCurrentTL = fl.getDocumentDOM().currentTimeline; 
fl.trace("The index of the current timeline is: "+ myCurrentTL);

The following example changes the active timeline from the main timeline to a scene named "myScene": var i = 0;
var curTimelines = fl.getDocumentDOM().timelines; 
while(i < fl.getDocumentDOM().timelines.length){
    if(curTimelines[i].name == "myScene"){ 
        fl.getDocumentDOM().currentTimeline = i;
    }
++i;
}

```
#### See also

[document.getTimeline()](../Document_object/docume88.md)
