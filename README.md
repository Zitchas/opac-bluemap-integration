# OpenPaC BlueMap - Remapped

This mod will show land claims from the [Open Parties and Claims](https://modrinth.com/mod/open-parties-and-claims) mod in the maps from the [BlueMap](https://modrinth.com/mod/bluemap) mod.

## Changes from the upstream versions

Originally, my motivation was the fact that I wanted the Claim highlighting to be fainter so that the underlying terrain was easier to see. Unfortunately, when I started working with it, I discovered that there was a build-breaking bug that was preventing it from building at all. Many thanks to Blue on the BlueMap discord for spotting the source of the problem: A single missing `"`.

As such, there are currently three differences between this and the upstream version:
- The missing `"` has been added, so the source code will now build properly.
- The claim line opacity has been reduced from 255 to 200.
- The claim fill opacity has been reduced from 102 to 64.

To-do:
- (necessary) Update versioning and title to reflect that this is more of an alternate BlueMap integration rather than an updated one. The upstream version still works as of Minecraft 1.21.10, after all.
- (optional) Update gradle to remove depreciated build code so it is gradle 9.x compatible.
- (goal) Figure out a way to move the opacities into the configuration file so they can be set by the server admin instead of needing to re-build the plugin.

## Will you support \<Version\>?

Probably, please open an issue.

## Usage

Simply install both the Open Parties and Claims mod as well as the BlueMap mod (and this mod), and you should be all set!
