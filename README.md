# cmoc-integration-visual-studio-code
Integration of CMOC (a Tandy Colour Computer C compiler) with Microsft Visual Studio Code IDE

The configuration assumes a project folder structure like this:

/PROJECT NAME
----/bin
----/src
----/include
----/lib
----/.vscode

copy the integration files available on this repository to the .vscode folder under the project folder.

Each and every project needs to have a .vscode folder under it. Copy the files to every new project folder.

to compile a file: Terminal >> Run Task >> CMOC - compile active file - target CoCo
this assumes the .c file is located in the src. The file needs to be open on Visual Studio Code.

to build a file: Terminal >> Run Task >> CMOC - build active file - targer CoCo
before building, makes sure to open the tasks.json file and adjust the last build task argument. It is the -l parameter. If any library needs to be included in the build than the library name needs to be added. example: -lbgraph. If no library needs to be included, remove the parameter.

to run a file: 
Debug >> Start without Debugging.


Assumptions:
in tasks.json - cmoc location :: C:\\cygwin64\\usr\\local\\bin\ - change to match your own setup
in launch.json - xroar location :: C:\\CODING\\TRSCOLOR\\xroar-0.35.2-w64\\xroar - change to match your own setup
in c_cpp_properties.json - include path for cmoc default libraries :: C:\\cygwin64\\usr\\local\\bin\\share\\cmoc\\include - change to match your own setup 

Requirements:
C/C++ for Visual Studio Code extension - extension identified: ms-vscode.cpptools

