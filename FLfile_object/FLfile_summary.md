## FLfile summary

#### Availability

Flash MX 2004 7.2.

#### Description

The FLfile object lets you write Flash extensions that can access, modify, and remove files and folders on the local file system. The FLfile API is provided in the form of an extension to the JavaScript API. This extension is called a *shared library* and is located in the following folder:

-   Windows 7 and 8:

*boot drive*\\Users\\*username*\\AppData\\Local\\Adobe\\Flash CC\\*language*\\Configuration\\External Libraries\\FLfile.dll

-   Mac OS X:

Macintosh HD/Users/*username*/Library/Application Support/Adobe/Flash CC/*language*/Configuration/External Libraries/FLfile.dll

***Note:** Don't confuse the shared libraries that contain symbols in your Flash documents with the JavaScript API shared libraries. They are two different things.*

The FLfile methods work with files or folders (directories) on disk. Therefore, each method takes one or more parameters to specify the location of a file or folder. The location of the file or folder is expressed as a string in a form very similar to a website URL. It is called a file URI (Uniform Resource Identifier) and is formatted as shown here (including the quote marks):

*"file:///drive\|/folder 1/folder 2/.../filename"*

For example, if you want to create a folder on the C drive called config and place it in the Program Files/MyApp folder, use the following command:

*FLfile.createFolder("file:///C\|/Program Files/MyApp/config");*

If you then want to place a file called config.ini in that folder, use the following command:

*FLfile.write("file:///C\|/Program Files/MyApp/config/config.ini", "");*

To create a folder on the Macintosh, you could use the following command:

*FLfile.createFolder("file:///Macintosh/MyApp/config");*

#### Method summary

The following methods can be used with the FLfile object:

| **Method**                             | **Description**                               |
|----------------------------------------|-----------------------------------------------|
| [FLfile.copy()](../FLfile_object/FLfile.md)        | Copies a file.                                |
| [FLfile.createFolder()](../FLfile_object/FLfile1.md) | Creates one or more folders.                  |
| [FLfile.exists()](../FLfile_object/FLfile2.md)       | Determines the existence of a file or folder. |

| **Method**                                       | **Description**                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [FLfile.getAttributes()](../FLfile_object/FLfile3.md)          | Finds out whether a file is writable, read-only, hidden, visible, or a system folder.                             |
| [FLfile.getCreationDate()](../FLfile_object/FLfile4.md)        | Specifies how many seconds have passed between January 1, 1970 and the time the file or folder was created.       |
| [FLfile.getCreationDateObj()](../FLfile_object/FLfile5.md)     | Gets the date a file or folder was created.                                                                       |
| [FLfile.getModificationDate()](../FLfile_object/FLfile6.md)    | Specifies how many seconds have passed between January 1, 1970 and the time the file or folder was last modified. |
| [FLfile.getModificationDateObj()](../FLfile_object/FLfile7.md) | Gets the date a file or folder was last modified.                                                                 |
| [FLfile.getSize()](../FLfile_object/FLfile8.md)                | Gets the size of a file.                                                                                          |
| [FLfile.listFolder()](../FLfile_object/FLfile9.md)             | Lists the contents of a folder.                                                                                   |
| [FLfile.platformPathToURI()](../FLfile_object/FLfile10.md)      | Converts a filename in a platform-specific format to a file:/// URI.                                              |
| [FLfile.read()](../FLfile_object/FLfile11.md)                   | Reads the contents of a file.                                                                                     |
| [FLfile.remove()](../FLfile_object/FLfile12.md)                 | Deletes a file or folder.                                                                                         |
| [FLfile.setAttributes()](../FLfile_object/FLfile13.md)          | Makes a file or folder read-only, writable, hidden, or visible.                                                   |
| [FLfile.uriToPlatformPath()](../FLfile_object/FLfile14.md)      | Converts a filename expressed as a file:/// URI to a platform- specific format.                                   |
| [FLfile.write()](../FLfile_object/FLfile15.md)                  | Creates, writes to, or appends to a file.                                                                         |

<span id="FLfile.copy()" class="anchor"></span>

