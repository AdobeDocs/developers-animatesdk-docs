## symbolInstance.tabIndex

#### Availability

Flash MX 2004.

#### Usage

symbolInstance.tabIndex

#### Description

Property; an integer that is equivalent to the Tab index field in the Accessibility panel. Creates a tab order in which objects are accessed when the user presses the Tab key. This property is not available for graphic symbols.

#### Example

The following example sets the tabIndex property of the mySymbol object to 3 and displays that value in the Output panel:

```javascript
var mySymbol = fl.getDocumentDOM().selection[0]; 
mySymbol.tabIndex = 3; 
fl.trace(mySymbol.tabIndex);

```