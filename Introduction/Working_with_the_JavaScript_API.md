## Working with the JavaScript API

As a user of Adobe® Animate®, you may be familiar with Adobe® ActionScript®, which lets you create scripts that execute at run time in Adobe® Flash® Player. The Animate JavaScript application programming interface (JavaScript API or JSAPI) described in this document is a complementary programming tool that lets you create scripts that run in the Animate authoring environment.

This document describes the objects, methods, and properties available in the JavaScript API. It assumes that you know how to use the documented commands when working in the authoring environment. If you have a question about what a particular command does, use other documents in Animate Help, such as *Using Animate*, to find that information.

This document also assumes that you are familiar with JavaScript or ActionScript syntax and with basic programming concepts such as functions, parameters, and data types.

The Animate JavaScript API lets you write scripts to perform several actions in the Animate authoring environment (that is, while a user has the Animate program open). This functionality is different from the ActionScript language, which lets you write scripts to perform actions in the Flash Player environment (that is, while a SWF file is playing). This functionality is also different from JavaScript commands that you might use in pages displayed in a web browser.

Using the JavaScript API, you can write Animate application scripts to help streamline the authoring process. For example, you can write scripts to automate repetitive tasks or add custom tools to the Tools panel.

The Animate JavaScript API is designed to resemble the Adobe® Dreamweaver® and Adobe® Fireworks® JavaScript API (which were designed based on the Netscape JavaScript API). The Animate JavaScript API is based on a Document Object Model (DOM), which allows Animate documents to be accessed using JavaScript objects. The Animate JavaScript API includes all elements of the Netscape JavaScript API, plus the Animate DOM. These added objects and their methods and properties are described in this document. You can use any of the elements of the native JavaScript language in an Animate script, but only elements that make sense in the context of an Animate document have an effect.

The JavaScript API also contains methods that let you implement extensibility using a combination of JavaScript and custom C code. For more information, see [C-Level Extensibility](#!AdobeDocs/developers-animatesdk-docs/test/C-Level_Extensibility/About_extensibility.md).

The JavaScript interpreter in Animate is the Mozilla SpiderMonkey engine, version 1.8, which is available on the web at [www.mozilla.org/js/spidermonkey/](http://www.mozilla.org/js/spidermonkey/). SpiderMonkey is one of the two reference implementations of the JavaScript language developed by Mozilla.org. It is the same engine that is embedded in the Mozilla browser.

SpiderMonkey implements the core JavaScript language as defined in the ECMAScript (ECMA-262) edition 3 language specification and it is fully compliant with the specification. Only the browser-specific host objects, which are not part of the ECMA-262 specification, are not supported. Similarly, many JavaScript reference guides distinguish between core JavaScript and client-side (browser-related) JavaScript. Only core JavaScript applies to the Animate JavaScript interpreter.

### Creating JSFL files

You can use Adobe Animate Professional or your preferred text editor to write and edit Animate JavaScript (JSFL) files. If you use Animate, these files have a .jsfl extension by default. To write a script, select File > New > Advanced > JSFL Script File.

You can also create a JSFL file by selecting commands in the History panel. Then click the Save button in the History panel or select Save As Command from the panel menu. The command (JSFL) file is saved in the Commands folder ([see Saving JSFL files](#saving-jsfl-files)). You can then open the file and edit it the same as any other script file.

The History panel provides some other useful options as well. You can copy selected commands to the Clipboard, and you can view JavaScript commands that are generated while you are working in Animate.

#### To copy commands from the History panel to the clipboard:

1.  Select one or more commands in the History panel.

2.  Do one of the following:

    -   Click the Copy button.

    -   Select Copy Steps from the panel menu.

#### To view JavaScript commands in the History panel:

-   Select View > JavaScript in Panel from the panel menu.

### Saving JSFL files

You can have JSFL scripts available within the Animate authoring environment by storing them in one of several folders within the Configuration folder. By default, the Configuration folder is in the following location:

-   Windows® 10™:

*boot drive*\\Users\\*username*\\AppData\\Local\\Adobe\\Animate *version*\\*language*\\Configuration\\

-   Mac OS® X:

Macintosh HD/Users/*username*/Library/Application Support/Adobe/Animate *version*/*language*/Configuration/

To determine the location of the Configuration folder, use [fl.configDirectory](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl12.md) or [fl.configURI](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl13.md), as shown in the following example:

```javascript
// store directory to a variable 
var configDir = fl.configDirectory;
// display directory in the Output panel 
fl.trace(fl.configDirectory);
```

Within the Configuration folder, the following folders can contain scripts that you can access in the authoring environment: Behaviors (to support the user interface for behaviors); Commands (for scripts that appear on the Commands menu); JavaScript (for scripts used by Script Assist to populate the user interface controls); Tools (for extensible tools in the Tools panel); and WindowSWF (for panels that appear in the Windows menu). This document focuses on scripts used for commands and tools.

If you edit a script in the Commands folder, the new script is immediately available in Animate. If you edit a script for an extensible tool, close and restart Animate, or else use the [fl.reloadTools()](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl57.md) command. However, if you used a script to add an extensible tool to the Tools panel and you then edit the script, either remove and then add the tool to the Tools panel again, or else close and restart Animate for the revised tool to be available.
There are two locations where you can store command and tool files so they can be accessed in the authoring environment.

-   For scripts that appear as items in the Commands menu, save the JSFL file in the Commands folder in the following location:

<table>
    <thead>
        <tr class="header">
            <th>
                <p><strong>Operating system</strong></p>
            </th>
            <th>
                <p><strong>Location</strong></p>
            </th>
        </tr>
    </thead>
    <tbody>
        <tr class="odd">
            <td>
                <p>Windows 10</p>
            </td>
            <td>
                <p><em>boot drive</em>\Users\<em>username</em>\AppData\Local\Adobe\Animate <em>version</em>\<em>language</em>\Configuration\Commands</p>
            </td>
        </tr>
        <tr class="even">
            <td>
                <p>Mac OS X</p>
            </td>
            <td>
                <p>Macintosh HD/Users/<em>userName</em>/Library/Application Support/Adobe/Animate <em>version/language</em>/Configuration/Commands</p>
            </td>
        </tr>
    </tbody>
</table>

-   For scripts that appear as extensible tools in the Tools panel, save the JSFL file in the Tools folder in the following location:

<table>
    <thead>
        <tr class="header">
            <th>
                <p><strong>Operating system</strong></p>
            </th>
            <th>
                <p><strong>Location</strong></p>
            </th>
        </tr>
    </thead>
    <tbody>
        <tr class="odd">
            <td>
                <p>Windows 10</p>
            </td>
            <td>
                <p><em>boot drive</em>\Users\<em>username</em>\AppData\Local\Adobe\Animate <em>version</em>\<em>language</em>\Configuration\Tools</p>
            </td>
        </tr>
        <tr class="even">
            <td>
                <p>Mac OS X</p>
            </td>
            <td>
                <p>Macintosh HD/Users/<em>userName</em>/Library/Application Support/Adobe/Animate <em>CC/language</em>/Configuration/Tools</p>
            </td>
        </tr>
    </tbody>
</table>

If a JSFL file has other files that go with it, such as XML files, store them in the same directory as the JSFL file.

### Running scripts

There are several ways to run scripts. The most common ways are explained in this section.

#### To run a script that you are currently viewing or editing:

-   Right-click (Command-click on the Macintosh) and choose Run Script.

-   Click the Run Script icon on the Script window toolbar.

This option lets you run a script before you have saved it. This option also lets you run a script even if no FLA files are open.

#### To run a script that is in the Commands folder, do one of the following:

-   From the authoring environment, select Commands > *Script Name*.

-   Use a keyboard shortcut that you have assigned to the script. To assign a keyboard shortcut, use Edit > Keyboard Shortcuts and select Drawing Menu Commands from the Commands pop-up menu. Expand the Commands node in the menu tree to view a list of available scripts.

#### To run a command script that is not in the Commands folder, do one of the following:

-   From the authoring environment, select Commands > Run Command, and then select the script to run.

-   From within a script, use the [fl.runScript()](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl62.md) command.

-   From the file system, double-click the script file.

#### To add a tool implemented in a JSFL file to the Tools panel:

1.  Copy the JSFL file for the tool and any other associated files to the Tools folder (see ["Saving JSFL files"](#saving-jsfl-files)).

2.  Select Edit  > Customize Tools Panel (Windows) or Animate > Customize Tools Panel (Macintosh).

3.  Add the tool to the list of available tools.

4.  Click OK.

You can add individual JavaScript API commands to ActionScript files by using the MMExecute() function, which is documented in the *ActionScript 3.0 Language and Components Reference*. However, the MMExecute() function has an effect only when it is used in the context of a custom user interface element, such as a component Property inspector, or a SWF panel within the authoring environment. Even if called from ActionScript, JavaScript API commands have no effect in Flash Player or outside the authoring environment.

#### To issue a command from an ActionScript script:

-   Use the following syntax (you can concatenate several commands into one string):
```
MMExecute(Javascript command string);
```
You can also run a script from the command line.

#### To run a script from the command line on Windows:

-   Use the following syntax (add path information as required):
```
"Animate.exe" myTestFile.jsfl [-AlwaysRunJSFL]
```
Use the `-AlwaysRunJSFL` option to bypass the dialog box that prompts you to confirm script execution.

#### To run a script from the "Terminal" application on the Macintosh, use either of the following:

-   Use the following osacript syntax (add path information as required):
```
osascript -e 'tell application "Animate" to open alias "Mac OS X:Users:user:myTestFile.jsfl" '
```
The osascript command can also run AppleScript in a file. For example, you could include the following text in a file named myScript:
```
tell application "Animate"
open alias "Mac OS X:Users:user:myTestFile.jsfl" 
end tell
```
Then, to run the script, you would use this command:
osascript myScript

-   Use the Animate command:
```
/Applications/Adobe\ Animate\ 2020/Animate.app/Contents/MacOS/Animate \<path of the jsfl file\>
```
