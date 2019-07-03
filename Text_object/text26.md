## text.tabIndex

#### Availability

Flash MX 2004.

#### Usage

text.tabIndex

#### Description

Property; an integer that is equivalent to the Tab Index field in the Accessibility panel. This value lets you determine the order in which objects are accessed when the user presses the Tab key.

#### Example

```
The following example gets the tabIndex of the currently selected object: var theTabIndex = fl.getDocumentDOM().selection\[0\].tabIndex; The following example sets the tabIndex of the currently selected object: fl.getDocumentDOM().selection\[0\].tabIndex = 1;

```