# C Makefile

## Instructions
It will compile your code but in order to work you have to have an header (.h) file for each source (.c) files

Target name can be changed in the makefile as all the directories names

## Rules
- **make** : will compile all the source files in object files and then create the final bin file
- **make init** : create all the directories of the workspace
- **make clean** : delete builds and bin files
- **make cleanBin** : delete bin files
- **make cleanBuild** : delete build files

## Directories
  If each directories names can be changed in the makefile there is the default structure of the workspace :
  
  |-src : to put source code (.c files)
  
  |-header : to put header files (.h files)
  
  |-build : where the object files will be created (.o files)
  
  |-bin : where final executable file will be placed (no extension)
