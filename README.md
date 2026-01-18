# OpenPaC BlueMap - Remapped

This mod will show land claims from the [Open Parties and Claims](https://modrinth.com/mod/open-parties-and-claims) mod in the maps from the [BlueMap](https://modrinth.com/mod/bluemap) mod.

## Changes from the upstream versions

Originally, my motivation was the fact that I wanted the Claim highlighting to be fainter so that the underlying terrain was easier to see. Unfortunately, when I started working with it, I discovered that there was a build-breaking bug that was preventing it from building at all. Many thanks to Blue on the BlueMap discord for spotting the source of the problem: A single missing `"`.

As such, there are currently three differences between this and the upstream version:
- The missing `"` has been added, so the source code will now build properly.
- The claim line opacity has been reduced from 255 to 200.
- The claim fill opacity has been reduced from 102 to 64.
- Both the line opacity and fill opacity values are now stored in the config file, and can be changed to any other integer between 0 and 255. This may need restarting the server to apply. Smaller values are fainter.

To-do:
- (necessary) Update versioning and title to reflect that this is more of an alternate BlueMap integration rather than an updated one. The upstream version still works as of Minecraft 1.21.10, after all.
- (optional) Update gradle to remove depreciated build code so it is gradle 9.x compatible.

## Will you support \<Version\>?

Probably, please open an issue.

Note: The current version was tested on Minecraft 1.21.10, and works perfectly.

## Usage

Simply install both the Open Parties and Claims mod as well as the BlueMap mod (and this mod), and you should be all set!

## Configuration

All of the following can be configured in the configuration file. The explanation is pulled from the file itself, it is just re-arranged and included here for ease of reference:

updateInterval: 12000,
	How often, in ticks, the markers should be refreshed. Set to 0 to disable automatic refreshing.
	Default is 10 minutes (12000 ticks).

markerMinY: 75.0,
markerMaxY: 75.0,
	The min and max Y for the markers. If these are the same, the marker will be drawn as a flat plane.
	Default is 75 to 75.

depthTest: false,
	If set to false, the markers won't be covered up by objects in front of it.
	Default is false.

lineOpacity: 200
fillOpacity: 1
	These two values set the opacity of the line and fill respectively, and can range from 0 to 255
	Default is 200 for the line and 64 for the fill.
	Note that in the upstream version of this plugin the values are 255 and 102 respectively, which are quite a bit more opaque.
