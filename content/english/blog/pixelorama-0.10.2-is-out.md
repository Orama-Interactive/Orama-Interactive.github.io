---
title: "Pixelorama v0.10.2 is out & Voxelorama is open-sourced!"
date: 2022-08-18T15:53:26+03:00
author: Emmanouil Papadeas
image: images/blog/pixelorama-0.10.2-is-out/main.png
---
Artwork by [Uch](https://www.instagram.com/vs.pxl/), one of the artists for v0.10's splash screen artworks.

Today is a special day for Pixelorama. Exactly three years ago, version 0.1 was released and the project was open sourced! To celebrate Pixelorama's 3rd birthday, we have not one, but two presents for you!

First of all, we are releasing a new version of Pixelorama, 0.10.2. While it's not a huge update in terms of new features, it is bringing huge performance increases and bug fixes, so it is highly recommended that you update. Keep reading to see the entire list of the changes.

Before we get to the second present, we would just like to remind you that if you wish to support us, you can [become a Patron](https://www.patreon.com/OramaInteractive) and receive exclusive awards, or [buy Pixelorama from itch.io](https://orama-interactive.itch.io/pixelorama)!

As for the second present... We have kept our promise, and we have finally open sourced Voxelorama! This means that it is now available for free for all of you, licensed under the MIT license, the same license as Pixelorama's. The project's code is [available on GitHub](https://github.com/Orama-Interactive/VoxeloramaExtension). Please note that Voxelorama is still in Early Access and is not recommended for production yet. Feedback and contributions are welcome, of course!

The changes that have arrived in Pixelorama v0.10.2 include:
### Added
- A gradient map image effect. Addresses the second half of [#595](https://github.com/Orama-Interactive/Pixelorama/discussions/595).
- A new rotation type, Rotxel with smear. Thanks to [azagaya](https://github.com/azagaya) for the shader code.
- The pivot in the rotate image dialog can now be changed by the user. [#720](https://github.com/Orama-Interactive/Pixelorama/pull/720)
- New offset options in tile mode that allow for non-rectangular tiling. [#707](https://github.com/Orama-Interactive/Pixelorama/pull/707)
- A basic API for Extensions. Has not been documented yet and is stil experimental.
- A similarity option in the Select by Color tool. [#710](https://github.com/Orama-Interactive/Pixelorama/pull/710)
- The left and right tool colors in the background of the tool buttons and the indicators on the canvas can now be changed from the Preferences.
- Added Danish translations.

### Changed
- Copying now works between multiple Pixelorama instances, and the clipboard is even being remembered when the app closes. Note that you cannot copy image data to another software, and you cannot paste image data from another software into Pixelorama. [#693](https://github.com/Orama-Interactive/Pixelorama/pull/693)
- Importing multiple images at once from File, Open is now possible.
- On image effect dialogs, the preview will show all of the selected cels instead of only one cel. [#722](https://github.com/Orama-Interactive/Pixelorama/pull/722)
- The indicator for the right tool is now enabled and orange by default.
- On quit, the "Save & Exit" button is now focused by default.
- The icon for onion skinning options has changed. [#711](https://github.com/Orama-Interactive/Pixelorama/pull/711)
- Extensions are now being automatically reloaded if the user installs an already-existing extension, without the need to restart Pixelorama.
- Updated to Godot 3.5.

### Fixed
- Fixed a macOS crash on startup. [90d2473](https://github.com/Orama-Interactive/Pixelorama/commit/90d2473f5256425146a8c10f539b7737aa37fd23)
- Even-numbered thickness sizes on the rectangle and ellipse shape tools now work as expected. The thickness of the shapes no longer goes up by 2 pixels. [23f591a](https://github.com/Orama-Interactive/Pixelorama/commit/23f591a8626c12fd7e6344ab59f8e33b8d20cb99)
- [[Keychain](https://github.com/Orama-Interactive/Keychain)] Fixed issue with menu events being triggered by actions that are not exact matches. This means that, for example, "Control + Shift + S" will no longer activate both "Save" and "Save as", but only "Save as". [09c9583](https://github.com/Orama-Interactive/Keychain/commit/09c95835ef034effa949732cf9cf9bd315ed08a8)
- Massively improved the performance of the selection system, most notably the Rectangle Selection and Select by Color tools, and selection content deletion. [#710](https://github.com/Orama-Interactive/Pixelorama/pull/710)
- Performance when drawing big lines on big canvases has been increased, thanks to the update to Godot 3.5. Most likely due to [godotengine/godot#62826](https://github.com/godotengine/godot/pull/62826)
- Fixed issue with save file dialog taking the name of the first file it sees. [5d65e82](https://github.com/Orama-Interactive/Pixelorama/commit/5d65e820708ed7586fdb7f0ac4633f7b468ec73d)
- Fixed grid-based snapped movement when the offset of the grid was larger than the grid size. [#712](https://github.com/Orama-Interactive/Pixelorama/pull/712)
- Fixed the symmetry points being on the wrong location on project initialization. [f432def](https://github.com/Orama-Interactive/Pixelorama/commit/f432defd1f92fde0677a5d10fde87e5219e47065)
- The quick color picker shortcut of the shape tools is now mapped to the correct action. [55935bc](https://github.com/Orama-Interactive/Pixelorama/commit/55935bcfd2597b9fc6be94c40542934e5f99aefc)
- The canvas preview play button now respects frame tags.
- Implemented a crash protection measure when loading extensions. [#715](https://github.com/Orama-Interactive/Pixelorama/pull/715)
- Fixed a crash when importing a spritesheet as a new layer, undoing and then exporting. [dcebf89](https://github.com/Orama-Interactive/Pixelorama/commit/dcebf894bf14b7de371f4661ec80c5f158087a23)
- Window transparency now only affects the transparency of the Main Canvas's TabContainer. [#734](https://github.com/Orama-Interactive/Pixelorama/pull/734)

Thank you all so much for supporting us these three amazing years. We appreciate every and each one of you, with special thanks to our contributors, our translators and our [patrons](https://www.patreon.com/OramaInteractive)! With your love and support, we will keep preparing even more amazing stuff for you. Happy painting, and keep pixelating (and voxelating?) your dreams.

Pixelorama is available on [GitHub](https://github.com/Orama-Interactive/Pixelorama) and [Itch.io](https://orama-interactive.itch.io/pixelorama)!
