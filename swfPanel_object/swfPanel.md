## swfPanel.call()

#### Availability

Flash CS4 Professional.

#### Usage

swfPanel.call(request)

#### Parameters

**request** Parameters to pass to the function (see “Description” and “Example” below).

#### Returns

Either null or a string that is returned by the function call. The function result could be an empty string.

#### Description

Method; works in conjunction with the ActionScript ExternalInterface.addCallback() and MMExecute()
>
methods to communicate with the SWF panel from the authoring environment.

#### Example

```
The following example illustrates how to use ActionScript and JavaScript code to create a Window SWF panel and communicate with it from the authoring environment.

1.  Create an ActionScript 3.0 FLA file, set its color to a medium gray, and set its size to 400 pixels wide and 250 pixels high.

2.  Place a dynamic text box in the center of the Stage, set its Instance name to myTextField, and type the word "Status" in the text box.

3.  Set other text box properties similar to the following:

    -   Center aligned

    -   355 pixels wide and 46 pixels high

    -   Times New Roman font, 28 points, red

4.  Add the following ActionScript code:

// Here's the callback function to be called from JSAPI function callMeFromJavascript(arg:String):void
{
try {
var name:String = String(arg); myTextField.text = name;
} catch (e:Error) {
}
}
// Expose the callback function as "callMySWF" ExternalInterface.addCallback("callMySWF", callMeFromJavascript);
// run the JSAPI to wire up the callback
MMExecute("fl.runScript( fl.configURI + \\"WindowSWF/fileOp.jsfl\\" );");
MMExecute("fl.trace(\\"AS3 File Status Panel Initialized\\");");

1.  Save the file as fileStatus.fla, and publish the SWF file with the default Publish settings.

2.  Close Flash.

3.  Copy the fileStatus.swf file to the WindowSWF folder, which is a subfolder of the Configuration folder (see [“Saving JSFL files” on page 2](#_bookmark3)). For example, on Windows XP, the folder is in *boot drive*\\Documents and Settings\\*user*\\Local Settings\\Application Data\\Adobe\\Flash CS4\\*language*\\Configuration\\WindowSWF.

4.  Start Flash.

5.  Create a JSFL file with the following code:

function callMyPanel(panelName, arg)
{
if(fl.swfPanels.length \0){
for(x = 0; x \< fl.swfPanels.length; x++){
// look for a SWF panel of the specified name, then call the specified AS3

function

// in this example, the panel is named "test" and the AS3 callback is "callMySWF" if(fl.swfPanels\[x\].name == panelName) // name busted?
{
fl.swfPanels\[x\].call("callMySWF",arg); break;
}
}
}
else
fl.trace("no panels");
}
// define the various handlers for events
documentClosedHandler = function () { callMyPanel("fileStatus", "Document Closed");}; fl.addEventListener("documentClosed", documentClosedHandler );
var dater = "New Document";
documentNewHandler = function () { callMyPanel("fileStatus", dater );}; fl.addEventListener("documentNew", documentNewHandler );
documentOpenedHandler = function () { callMyPanel("fileStatus", "Document Opened");}; fl.addEventListener("documentOpened", documentOpenedHandler );

1.  Save the JSFL file in the same directory as the SWF file, with the name fileOp.jsfl.

2.  Choose Window \Other panels \fileStatus.

Now, as you create, open, and close FLA files, the fileStatus panel displays a message indicating the action you have taken.

```