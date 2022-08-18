---
title: "Pixelorama v0.10.1 is out!"
date: 2022-06-06T16:01:26+03:00
author: Emmanouil Papadeas
image: images/blog/pixelorama-0.10.1-is-out/main.png
---
Artwork by [Wishdream](https://twitter.com/WishdreamStar), one of the artists for v0.10's splash screen artworks.

We have amazing news for you! A new version of Pixelorama is releasing today, version 0.10.1, with some awesome new features and various changes. Along with that, we are also announcing **Voxelorama**, an extension for Pixelorama that converts your pixel art into voxel art. For more information on that, you can [read this blog post](../announcing-voxelorama).

If you wish to support us, you can [become a Patron](https://www.patreon.com/OramaInteractive) and receive exclusive awards, or [buy Pixelorama from itch.io](https://orama-interactive.itch.io/pixelorama)!

The changes that have arrived in v0.10.1 include:
### Added
- The [Keychain plugin](https://github.com/Orama-Interactive/Keychain) has been implemented. Keychain makes Pixelorama's shortcut system fully configurable, and it provides the ability to the users to set custom shortcuts of every input type for all input actions. The plugin is developed by us and it's free to use for your own Godot projects as well! [#700](https://github.com/Orama-Interactive/Pixelorama/pull/700)
- The cursor can now be moved with the numpad arrow keys and gamepad's left stick and d-pad, the canvas can be moved with gamepad's right stick and it is also possible to map the activate left and right tool actions to keyboard and gamepad buttons, to allow drawing from these devices, making Pixelorama a lot more accessible. Made possible by the Keychain plugin.
- A lot more gradient options have been added. Apart from the Linear Step gradient, there are now Linear, Radial, Radial Step, Linear Dithering and Radial Dithering gradient types. They are all shader-based, so they are a lot faster than the previous method. [#677](https://github.com/Orama-Interactive/Pixelorama/pull/677)
- A drop shadow image effect has been added. [#674](https://github.com/Orama-Interactive/Pixelorama/pull/674)
- A new rotation method has been added. It is shader-based, therefore faster than the other methods. [#683](https://github.com/Orama-Interactive/Pixelorama/pull/683)
- All menu items now have changeable shortcuts. Made possible by the Keychain plugin.
- The dimensions of the exported file(s) are now visible in the export dialog. [#686](https://github.com/Orama-Interactive/Pixelorama/pull/686)

### Changed
- The outline effect is now generated using shaders, except in the Web platform. This makes outline generation more faster and gives better results.
- In the backup confirmation dialog, "Delete" has been changed to "Discard all" and a Cancel button has been added.
- Grid, pixel grid, rulers and guides view menu settings are now being remembered when Pixelorama closes and opens again.
- The export window is now more clear if the directory path, the file name or both are invalid. [#669](https://github.com/Orama-Interactive/Pixelorama/pull/669)
- Timeline scroll behavior has been tweaked. [#682](https://github.com/Orama-Interactive/Pixelorama/pull/682)
- Image brush size is now using percentage suffix (%) instead of pixels (px). [#671](https://github.com/Orama-Interactive/Pixelorama/pull/671)
- The brushes popup tab alignment and position has changed depending on where it's asked to popup. [#671](https://github.com/Orama-Interactive/Pixelorama/pull/671)
- It is now possible to delete content from all selected cels.

### Fixed
- The flood fill algorithm (bucket tool's "same color area" mode) is now a lot faster. [#667](https://github.com/Orama-Interactive/Pixelorama/pull/667) and [#672](https://github.com/Orama-Interactive/Pixelorama/pull/672)
- Based on the above, the magic wand tool is also a lot faster.
- Shader-based image effects are now a lot faster if there is no selection.
- GIF exporting is now faster. [#696](https://github.com/Orama-Interactive/Pixelorama/pull/696)
- Fixed issue with the bucket tool's "same color pixels" method not working in all selected cels.
- Fixed broken 90-degree rotation. [#676](https://github.com/Orama-Interactive/Pixelorama/pull/676)
- Fixed export bug where the path is being changed if there's a folder with the same name as the file.
- Fixed visual bug caused by window opacity. [#680](https://github.com/Orama-Interactive/Pixelorama/pull/680)
- It is no longer possible to delete content from cels belonging to invisible or locked cels.
- Scale image aspect ratio is now updating correctly when the dialog is about to appear.
- Going into fullscreen mode and then exiting it no longer makes the window opacity not working properly. Note that window opacity still does not work when in fullscreen mode.

![Screenshot from Pixelorama's new gradient system](../../images/blog/pixelorama-0.10.1-is-out/gradients.png)
Screenshot from Pixelorama's new gradient system

Thank you all for taking the time to read this blog post and for supporting us. We appreciate every and each one of you, with special thanks to our contributors, our translators and our [patrons](https://www.patreon.com/OramaInteractive)! Happy painting, and keep pixelating your dreams.

Pixelorama is available on [GitHub](https://github.com/Orama-Interactive/Pixelorama) and [Itch.io](https://orama-interactive.itch.io/pixelorama)!
