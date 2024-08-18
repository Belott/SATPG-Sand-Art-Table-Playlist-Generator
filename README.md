# SATPG - Sand Art Table Playlist Generator
## Overview
With the Sand Art Table Playlist Generator (SATPG), you can quickly create playlists for the sand art table based on the IKEA Lack table and FluidNC firmware. With just a few clicks, you can arrange your best sand pictures in the perfect order. The graphic preview takes the specific properties of a sand art table into account in a way that no other GCODE simulator can. Export your playlist as a GCODE file and play it directly on the FluidNC firmware. This eliminates the need for GCODE players and similar tools.

## System Requirements
This is a .NET Desktop Application developed for the .NET Framework 8, requiring at least Windows 7 as the operating system.
SATPG creates GCODE files for the FluidNC firmware version 3.8 and higher.

## Installation

### Install .NET Framework 8
Before running the application, ensure that .NET Framework 8 is installed on your system. You can download .NET Framework 8 [here](https://dotnet.microsoft.com/en-us/download).

### Download and Run the Application
1. Download the latest version of the application from the [Releases page](https://github.com/Belott/SATPG-Sand-Art-Table-Playlist-Generator/releases).
2. Extract the downloaded file to a location of your choice.
3. Double-click the `SATPG.exe` file to start the application.

## Usage
### Video-Tutorial
Please check my Youtube channel to find more information about this tool and the sand art table: https://www.youtube.com/@BINGOBRICKS

### First Steps
1. Click on the "Load" button and select a directory that contains GCODE files of your sand images. (SATPG loads all GCODE files into the preselect collection.)
2. Select the images in the preview list that you want to include in the playlist and click on the arrow to the right.
3. Use the up/down arrows to arrange the GCODE files in the order you want them in the playlist.
4. Switch to the "Create" view.
5. Specify in the "Path on SD Card" field the directory in which the GCODE files will be located from the controller's perspective.
6. Click the "Save" button and enter a file name and storage location for your playlist. (SATPG will also copy all GCODE image files of your playlist into this folder and number them in order.)
7. Load all files created by SATPG to the SD card of your sand art table and play the playlist GCODE file.
8. Enjoy!

## Features
### Preselection
Create a preselection of your GCODE image files. You can add GCODE files from several directories to the preselection.

### Preview sand image 
SATPG's GCODE preview takes into account some special features that must be considered for sand art tables:
- A homing is interpreted as movement and is therefore visible with a line in the preview.
- The end point of the previous image of a playback sequence (where the ball comes to rest) is linked to the start point of the current image and is therefore drawn with a line in the preview.

Limitations of SATPG GCODE preview:
- Travel paths in relative mode (Command G91) are ignored, as these are usually not used for sand art tables.

### Random order
Mix your playlist with one click and put it in a random order.

### Multiple mention 
Copy GCODE files with one click to play your best images multiple times.

### Custom playlist header
Add a custom GCODE header to the playlist.

### Breaks
Automatically insert a G4 command between the sand images to pause between the images.

### Preview playlist GCODE
Preview the generated GCODE for the playlist.

### Copy und number
Copies all your GCODE image files to the destination directory and gives them a number in the playlist order.

## License
This application is licensed under the 'GPL-3.0' license. For more details, please see the `LICENSE` file.
