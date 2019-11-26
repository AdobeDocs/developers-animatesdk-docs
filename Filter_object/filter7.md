## filter.enabled

#### Availability

Flash CS3 Professional.

#### Usage

filter.enabled

#### Description

Property; a Boolean value that specifies whether the specified filter is enabled (true) or disabled (false).

#### Example

```javascript
The following example disables the Color filters on the selected object(s):
var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i < myFilters.length; i++){
if(myFilters[i].name == 'adjustColorFilter'){ myFilters[i].enabled = false;
}
}
fl.getDocumentDOM().setFilters(myFilters);

```