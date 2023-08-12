---
title: "Pixelorama v0.11.1 is out!"
date: 2023-08-12T14:00:00+03:00
author: Emmanouil Papadeas
image: images/blog/pixelorama-0.11.1-is-out/main.png
---
Artwork by [Wishdream](https://twitter.com/WishdreamStar), one of the artists for v0.11's splash screen artworks.

The 0.x versions haven't said their last word yet. Here comes version v0.11.1, with some new features and nice improvements to the user improvements.

Before we get to what is new in this version, in the last article we mentioned that the next major version of Pixelorama will most likely be v1.0. We are happy to tell you that we have started work on v1.0 by beginning the transition from Godot 3.5, the engine we use to develop Pixelorama, to Godot 4.1. And so far it's going very well! You can keep track of the progress in the new [godot4 branch on GitHub](https://github.com/Orama-Interactive/Pixelorama/tree/godot4). When the work is complete, we will merge the new code in to the main branch and delete the godot4 branch.

However, this won't mean that v1.0 will be out when the transition is complete. We want to take the time to add some more missing features and polish the overall application, so it can be ready for production use. We want version 1.0 to be considered ready to use for everyone, with as less problems as possible. This means that the next few months may seem quieter, as we will focus on developing v1.0 and not make any new updates until then, unless they are bug fixes. Please do not let this worry you, our silence doesn't mean that the project is inactive. The complete opposite, actually! And of course, you can always track our work on Pixelorama's GitHub.

We want version 1.0 to be as good as possible, and for it to come out as fast as possible. We know that this is what you want as well, so we could really use your help! If you wish to support us, you can [become a Patron](https://www.patreon.com/OramaInteractive) and receive exclusive awards, or [buy Pixelorama from itch.io](https://orama-interactive.itch.io/pixelorama)!

[![Become a patron](../../images/blog/become_a_patron.png)](https://patreon.com/OramaInteractive)

Enough about the future, let us focus on the present! Here is the full changelog of v0.11.1:

### Added
- A new offset image effect to easily move the image around, with animation support.
- Implemented a "smart slicer" system that lets the software automatically slice a spritesheet in separate frames on image import, without the user having to specify horizontal and vertical frames. [#893](https://github.com/Orama-Interactive/Pixelorama/pull/893)
- Added optional integer zooming for the canvas, which can be enabled from the Preferences. Disabled by default. [#894](https://github.com/Orama-Interactive/Pixelorama/pull/894)
- Fast way to clone frames of a tag. [#861](https://github.com/Orama-Interactive/Pixelorama/pull/861)
- Added a reverse frames option on the right click menu of the frame buttons, to easily reverse the order of the selected frames.
- A new Timeline category in the Preferences with options such as the colors of onion skinning's color mode, and whether a layer should be selected when a layer button (such as lock, visibility etc) gets pressed.
- It is now possible to disable saving frames that have a tag to a different folder, as well as specifying a separator character in the file names.
- Palette file types now exist as filters in the Open file dialog.
- .bmp and .tga file types now exist in the Open dialog of the Web version.

### Changed
- The image effect animation system introduced in v0.11 has been overhauled with a better user interface, and with tweening options. [#879](https://github.com/Orama-Interactive/Pixelorama/pull/879)
- Images stored in RAM for the undo/redo system when draw tools are used are now compressed. This reduces RAM usage. [#890](https://github.com/Orama-Interactive/Pixelorama/pull/890)
- The cel opacity slider now affects all of the selected cels. [#865](https://github.com/Orama-Interactive/Pixelorama/pull/865)
- The right click menu of the frame buttons now works for all selected frames, besides "move left" and "move right".
- The canvas is automatically enlarged when importing an image of a larger size to the project.
- Error codes are now being explained in the error messages. [#891](https://github.com/Orama-Interactive/Pixelorama/pull/891)
- Newly cloned frames are now automatically selected. [#861](https://github.com/Orama-Interactive/Pixelorama/pull/861)
- "Centralize Image" has been moved from the Image menu to the frame button right click menu. [#884](https://github.com/Orama-Interactive/Pixelorama/pull/884)
- The project's name is no longer saved inside .pxo files. Loaded projects now get their name directly from the file name.
- Clicking on a layer button (such as lock, visibility etc) no longer selects the layer by default. This behavior can now be changed in the Preferences.
- The image menu has been re-arranged. [#878](https://github.com/Orama-Interactive/Pixelorama/pull/878)
- The "OK" button of the save and export dialogs are now named "Save" and "Export" respectively. [#876](https://github.com/Orama-Interactive/Pixelorama/pull/876)

### Fixed
- Generating palettes from the current project no longer crashes when group and 3D layers exist.
- Fixed wrong saturation and value values. They were divided by 360, while they should have been divided by 100. [#879](https://github.com/Orama-Interactive/Pixelorama/pull/879)
- Fixed image effect animations appearing when changing the affected option, even if that image effect had no animatable properties. [#879](https://github.com/Orama-Interactive/Pixelorama/pull/879)

Thank you all for taking the time to read this blog post and for supporting us. We appreciate every and each one of you, with special thanks to our contributors, our translators and our [patrons](https://www.patreon.com/OramaInteractive)! Happy painting, and keep pixelating your dreams.

Pixelorama is available on [GitHub](https://github.com/Orama-Interactive/Pixelorama) and [Itch.io](https://orama-interactive.itch.io/pixelorama)!
