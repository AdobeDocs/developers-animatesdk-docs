## Sample implementations

Several sample JSFL implementations are available for Adobe Flash Professional CS5 and CS5.5. You can review and install these files to familiarize yourself with the JavaScript API. The samples are in a folder named Samples/ExtendingFlash within the Samples.zip file located at [www.adobe.com/go/learn\_fl\_samples](http://www.adobe.com/go/learn_fl_samples).

### Sample Shape command

A sample JavaScript API script named Shape.jsfl is located in the ExtendingFlash/Shape folder (see "Sample implementations" above). This script displays information about the contours of the shape in the Output panel.

#### To install and run the Shape script:

1.  Copy the Shape.jsfl file to the Configuration/Commands folder (see ["Saving JSFL files" on page 2](#_bookmark2)).

2.  In a Flash document (FLA file), select a shape object.

3.  Select Commands \Shape to run the script.

### Sample get and set filters command

A sample JavaScript API script named filtersGetSet.jsfl is located in the ExtendingFlash/filtersGetSet folder (see "Sample implementations" above). This script adds filters to a selected object and displays information about the filters being added in the Output panel.

#### To install and run the filtersGetSet script:

1.  Copy the filtersGetSet.jsfl file to the Configuration/Commands folder (see ["Saving JSFL files" on page 2](#_bookmark2)).

2.  In a Flash document (FLA file), select a text, movie clip, or button object.

3.  Select Commands \filtersGetSet to run the script.

### Sample PolyStar tool

A sample JavaScript API script named PolyStar.jsfl is located in the ExtendingFlash/PolyStar folder (see "Sample implementations" above).
The PolyStar.jsfl replicates the PolyStar tool that can be found in the Flash Tools panel. The script demonstrates how to build the PolyStar tool using the JavaScript API and includes detailed comments describing what the code is doing. Read this file to gain a better understanding of how the JavaScript API can be used. You should also read the PolyStar.xml file in the Tools directory to learn more about how to build your own tool.

### Sample Trace Bitmap panel

A set of files named TraceBitmap.fla and TraceBitmap.swf are located in the ExtendingFlash/TraceBitmapPanel folder (see "Sample implementations" above). These files illustrate how to design and build a panel to control the functions of Flash. They also show the use of the MMExecute() function to call JavaScript commands from an ActionScript script.

#### To run the TraceBitmap sample:

1.  If Flash is running, exit from Flash.

2.  Copy the TraceBitmap.swf file to the WindowSWF folder, which is a subdirectory of the Configuration folder (see ["Saving JSFL files" on page 2](#_bookmark2)). For example, on Windows XP, the folder is in *boot drive*\\Documents and Settings\\*user*\\Local Settings\\Application Data\\Adobe\\Flash CS5\\*language*\\Configuration\\WindowSWF.

3.  Start Flash.

4.  Create or open a Flash document (FLA file), and import a bitmap or JPEG image into the file.

You can use the flower.jpg file provided in the TraceBitmapPanel folder or another image of your choice.

1.  With the imported image selected, select Window \Other Panels \TraceBitmap.

2.  Click Submit.

The image is converted into a group of shapes.

### Sample DLL

A sample DLL implementation is located in the ExtendingFlash/dllSampleComputeSum folder (see "Sample implementations" above). For more information about building DLLs, se[e "C-Level Extensibility" on page 591](#_bookmark1165).

