---
title: "Pixelorama v0.11 is out!"
date: 2023-06-13T17:45:26+03:00
author: Emmanouil Papadeas
image: images/blog/pixelorama-0.11-is-out/main.png
---
Artwork by Exuvita, one of the artists for v0.11's splash screen artworks.

After almost nine months, a new version of Pixelorama, version 0.11, is finally out! It might seem like a long time without an update, but we have been working hard these months to make this update amazing, and we are proud to say that this is probably the biggest update so far! At least until version 1.0, which will most likely be the next major version of Pixelorama!

Another reason it took so long to release a new update was because we were very busy. My team and I were working on a freelance job in order to make money, which took some time from Pixelorama's development. Pixelorama is a passion project that we work on during our free time, but out free time is not as much as it used to be, so we could definitely use your help! If you wish to support the development process so we can spend more of our time on this amazing project (and future ones!), you can [become a Patron](https://www.patreon.com/OramaInteractive) and receive exclusive awards, or [buy Pixelorama from itch.io](https://orama-interactive.itch.io/pixelorama)! If you don't wish to support us, you can rest easy knowing that no matter what, we will still keep working on Pixelorama for the foreseeable future, and it will always remain free for everyone to use.

[![Become a patron](../../images/blog/become_a_patron.png)](https://patreon.com/OramaInteractive)

Here is an overview of the biggest changes that came with the new version.

## Timeline improvements
Thanks to [MrTriPie](https://github.com/mrtripie), one of Pixelorama's contributors, the timeline has been refactored behind the scenes. This resulted in a **massive** performance boost when a project has many frames and/or layers. The refactoring also allowed for some well needed feature additions, such as layer groups. Yes, long gone are the days where your timeline was a large pile of layers, with no way to organize them. Now, you can group them together! For more information, see [#698](https://github.com/Orama-Interactive/Pixelorama/pull/698).

## 3D layers
The timeline refactoring made it easy to add new layer types in the codebase. One of these new layer types is 3D layers, which made their way to v0.11.
![Screenshot from Pixelorama's new 3D layers](../../images/blog/pixelorama-0.11-is-out/3d_layers.png)

3D layers allow you to break the dimensional barrier, and bring 3D shapes and models into your 2D canvas. You can add a variety of 3D shapes, custom text, three types of lights or a completely custom .obj model, and Pixelorama will automatically pixelate it, depending on the size of your canvas. To help you edit your objects, a new 3D Shape Edit tool has been added, which is only available when a 3D layer is selected. You can use this tool to select an object and move it around, rotate it, scale it, or change any other property from the tool options. All of the editing is non-destructive. If you wish to edit them destructively, you can merge a 3D layer into a pixel layer that is below it, and you can use the familiar draw tools to edit the image to your liking.

This feature was inspired by certain 3D games that render their 3D geometry in such a way to achieve a pixel art look. 3D layes are still rather basic, and lack some features, such as materials, and the UI/UX still needs some work. It's also worth noting that 3D text is not meant to replace a proper text tool, which will be coming when we add vector layers. For more information, see [#840](https://github.com/Orama-Interactive/Pixelorama/pull/840).

## Reference images
Contributor [20kdc](https://github.com/20kdc) has added support for reference images to Pixelorama. This allows you to load any kind of image, even high-res images, and use them as references that can help you draw. The reference images are not being included when you export a file, and are not being saved in pxo files due to size reasons. For more information, see [#771](https://github.com/Orama-Interactive/Pixelorama/pull/771).

## Exporting improvements
The export dialog window has been overhauled to improve the user experience and to add some new features, such as specific layer exporting, more information at [#781](https://github.com/Orama-Interactive/Pixelorama/pull/781). v0.11 also comes with APNG (animated png) importing and exporting, thanks to [20kdc](https://github.com/20kdc).

## Perspective editor
Contributor [Variable](https://github.com/Variable-ind) has implemented a new perspective editor. This is very useful for artworks that use perspective, for a more 3D look. For more information, see [#806](https://github.com/Orama-Interactive/Pixelorama/pull/806).

## Dynamics
After a long time of being work in progress, dynamics, such as tablet pen pessure and mouse/pen velocity are finally here.

## Image effect improvements
Rotation now has two new shader-based algorithms, [cleanEdge](http://torcado.com/cleanEdge/) and [OmniScale](https://github.com/nobuyukinyuu/godot-omniscale). The latter is only available when using the GLES3 renderer. A new image effect, Posterize, has also been added, which is used to automatically reduce the colors of an image. Certain image properties can now also be animated for multiple cels, thanks to [Variable](https://github.com/Variable-ind). For more info see [#836](https://github.com/Orama-Interactive/Pixelorama/pull/836).

## New tools
Version 0.11 comes with new tools, a crop tool, added by [MrTriPie](https://github.com/mrtripie) in [#830](https://github.com/Orama-Interactive/Pixelorama/pull/830), which allows for easy canvas resizing, and a new select by drawing tool, added by [Variable](https://github.com/Variable-ind) in [#792](https://github.com/Orama-Interactive/Pixelorama/pull/792). Variable has also made some improvements in already-existing tools, such as adding a spacing option in the pencil tool ([#813](https://github.com/Orama-Interactive/Pixelorama/pull/813)), and adding a way to change the selection creation behavior for selection tools from the tool options ([#798](https://github.com/Orama-Interactive/Pixelorama/pull/798)).

## Recorder
Do you like creating art timelapses? [Variable](https://github.com/Variable-ind) has got you covered! This new version comes with a new recorder panel that you can use to automatically record your drawing progress. Pixelorma will save each action you do as a screenshot, which you can later combine into a video. The panel is not visible by default, so if you want to use this, you can go to the Window menu, and on the Panels submenu, click on "Recorder". In the future, we could make it so that a video is automatically being created, but that would require ffmpeg being installed on your device. More information at [#823](https://github.com/Orama-Interactive/Pixelorama/pull/823).

## Dropping support for Ubuntu Touch
Ubuntu Touch builds have stopped working for some time now, and because I have neither the knowledge nor the time to maintain this platform, I am afraid we have to drop support for it. If in the future supporting Ubuntu Touch becomes easier, or if Godot supports it out of the box, we may start supporting it again.

## Full changelog
### Added
- Layer groups in the timeline, for better organization. [#698](https://github.com/Orama-Interactive/Pixelorama/pull/698)
- Support for reference images has been implemented. [#771](https://github.com/Orama-Interactive/Pixelorama/pull/771)
- Specific layer exporting is now possible as part of the export dialog overhaul. [#781](https://github.com/Orama-Interactive/Pixelorama/pull/781)
- 3D layers have now been implemented, which allows for non-destructive usage of 3D geometry inside Pixelorama. The 3D objects get automatically rasterized (pixelated) depending on the size of the canvas. [#840](https://github.com/Orama-Interactive/Pixelorama/pull/840)
- A perspective editor has been added, that aims to help artists use perspective in their work. [#806](https://github.com/Orama-Interactive/Pixelorama/pull/806)
- Dynamics are finally here! You can now use tablet pen pressure and/or mouse/pen velocity to affect the size and the alpha of the brush. More options will come in the future!
- A new crop tool has been added. It can resize the canvas without resizing the content. [#830](https://github.com/Orama-Interactive/Pixelorama/pull/830)
- The pencil tool now has a spacing option. [#813](https://github.com/Orama-Interactive/Pixelorama/pull/813)
- Exporting and loading APNG files is now possible. [#772](https://github.com/Orama-Interactive/Pixelorama/pull/772) and [#797](https://github.com/Orama-Interactive/Pixelorama/pull/797)
- Implemented [cleanEdge](http://torcado.com/cleanEdge/) as a new rotation and scaling algorithm. [#794](https://github.com/Orama-Interactive/Pixelorama/pull/794)
- [GLES 3 only] Implemented [OmniScale](https://github.com/nobuyukinyuu/godot-omniscale) as a new rotation and scaling algorithm. [08e00d3](https://github.com/Orama-Interactive/Pixelorama/commit/08e00d3c31dd134be037b672b7ac1d192400ac4d)
- Added a new Posterize image effect, with optional dithering. It's used to automatically reduce colors of an image.
- A new select by drawing tool has been added. [#792](https://github.com/Orama-Interactive/Pixelorama/pull/792)
- Some image effect properties can now be animated for multiple cels. [#836](https://github.com/Orama-Interactive/Pixelorama/pull/836)
- It is now possible to change the selection creation behavior (replace, add, subtract or intersect) from the tool settings. [#798](https://github.com/Orama-Interactive/Pixelorama/pull/798)
- Your art progress inside Pixelorama can now be recorded and saved as screenshots, for you to combine into a video. Useful for art timelapses. [#823](https://github.com/Orama-Interactive/Pixelorama/pull/823)
- Control + Mouse wheel can now be used to adjust the brush size and shape thickness. Unfortunately, this shortcut cannot be edited at the moment, but it will be in the future (most likely once we port to Godot 4.x). [#776](https://github.com/Orama-Interactive/Pixelorama/discussions/776)
- Snapping to the grid and guides has been implemented.
- Changing the renderer from GLES2 to GLES3 and vice versa is now possible in the preferences.
- Selections now have their own tile mode option, that works within the boundaries of the selection. [#834](https://github.com/Orama-Interactive/Pixelorama/pull/834)
- A way to easily preview an animation that has frames drawn in the form of a spritesheet/atlas has been added in the canvas preview. [#835](https://github.com/Orama-Interactive/Pixelorama/pull/835)
- The average color between the two selected colors is now shown in the color pickers, and can be easily picked. [#822](https://github.com/Orama-Interactive/Pixelorama/pull/822)
- A list of the recently used project sizes now appears on the new project dialog. [#819](https://github.com/Orama-Interactive/Pixelorama/pull/819)
- [Windows only] Changing the tablet driver is now possible in the preferences.

### Changed
- The palette panel is now more reactive; it automatically resizes in order to show/hide swatches based on its size. It is also now possible to scroll palettes with the mouse wheel, and resize the swatches with Control + mouse wheel. [#761](https://github.com/Orama-Interactive/Pixelorama/pull/761)
- The UI of the animation timeline has been improved. [#769](https://github.com/Orama-Interactive/Pixelorama/pull/769)
- The entire export dialog UI has been overhauled. [#781](https://github.com/Orama-Interactive/Pixelorama/pull/781)
- Linked cels have been refactored, which allows for having multiple linked sets of cels in the same layer. [#764](https://github.com/Orama-Interactive/Pixelorama/pull/764)
- Most Slider + SpinBox combinations have been replaced by a custom slider, made by [@mrtripie](https://github.com/mrtripie).
- Gradient generation is now more powerful; there is now support for multi-color gradients and they can be repeated. Step gradients have been removed in favor of linear gradients with constant interpolation.
- The color picker now picks any visible color on the canvas, regardless of layer. A toggle has also been added in the tool options to let the user change back to the previous behavior of only picking a color on the selected layer. [#816](https://github.com/Orama-Interactive/Pixelorama/pull/816)
- A single popup appears when exporting multiple files that already exist, instead of showing one popup for each file to overwrite. [#585](https://github.com/Orama-Interactive/Pixelorama/discussions/585)
- Most dialogs received some UI changes, such as making their elements expand vertically, and making their Cancel and OK buttons a little bigger.
- The look of the brushes popup has been improved. [#815](https://github.com/Orama-Interactive/Pixelorama/pull/815)
- The cel buttons on the timeline are now dimmed if the cel is empty/transparent.
- The manage layout dialog now has a preview for the selected layout. [#787](https://github.com/Orama-Interactive/Pixelorama/pull/787)
- Layer adding behavior has been changed. [#767](https://github.com/Orama-Interactive/Pixelorama/pull/767)
- The canvas rulers can now display floating point numbers. [#800](https://github.com/Orama-Interactive/Pixelorama/pull/800)
- The tile mask, used in tile mode, is now being set automatically. [#833](https://github.com/Orama-Interactive/Pixelorama/pull/833)
- When having multiple cels selected and onion skinning is enabled, using the Move tool now also has an immediate visible effect on the onion skinning preview. [#862](https://github.com/Orama-Interactive/Pixelorama/pull/862)
- Onion skinning settings are now being saved and are remembered between sessions. [#857](https://github.com/Orama-Interactive/Pixelorama/pull/857)
- Contributors and donors in the About dialog are now sorted in alphabetical order.

### Fixed
- The timeline has been refactored behind the scenes, and its performance has been massively improved for projects with a lot of frames and layers. [#698](https://github.com/Orama-Interactive/Pixelorama/pull/698)
- If Pixelorama crashes during saving of a .pxo file and a file of the same name already exists in that directory, it no longer gets replaced with an empty 0 byte file. [#763](https://github.com/Orama-Interactive/Pixelorama/issues/763)
- [macOS] Fixed issue where tool shortcuts changed tools. [#784](https://github.com/Orama-Interactive/Pixelorama/pull/784)
- The movement preview now works as intended for all selected cels [#811](https://github.com/Orama-Interactive/Pixelorama/pull/811) for the move tool, [5cb0edd](https://github.com/Orama-Interactive/Pixelorama/commit/5cb0eddae5983b29a378a34ad4919116f911a403) for the selected content.
- The UI scale no longer is 0.75 by default. This fixes blurry fonts on small monitors.
- Opening the rotate image dialog twice on large canvases no longer results in a crash. [ad61ddc](https://github.com/Orama-Interactive/Pixelorama/commit/ad61ddc2c0c251e8e20da3369c072e48380c0cd3)
- Pasted content should no longer get placed in sub-pixel positions. [403539b](https://github.com/Orama-Interactive/Pixelorama/commit/403539bb4794d81289214c4eda5226e70b9af19a)
- The notifications always appear on the bottom left of the main canvas and are no longer dependent on the position of the timeline.
- The recent files option in the File menu is now disabled in the Web version, instead of save.
- Drawing with image brushes no longer results in pixels outside the selection, if it exists. [30d279c](https://github.com/Orama-Interactive/Pixelorama/commit/30d279c4948b5712dac87bf6575932ca30d1c4dc)
- Using the selection gizmos when an overlay window is directly on top of them is no longer possible.
- Fix bug where the tool changes from a draw tool to a non-draw tool, while having an image brush selected. The bug was that the indicator was appearing as a white square, until the user moved their mouse.
- Fix bug where clicking on previous/next frame when only one frame exists makes the cel unselected. [6b58768](https://github.com/Orama-Interactive/Pixelorama/commit/6b587688f12dcc027c2f43832f179e4dca73a702)
- Mirror symmetry axes are now properly centered by default. [#843](https://github.com/Orama-Interactive/Pixelorama/pull/843)
- The "File(s) exported" notification now only appears on successful export.
- Fix selection handles and shape tool previews not working properly when mirror view is enabled. [#860](https://github.com/Orama-Interactive/Pixelorama/pull/860)
- Undoing after pasting now shows the previous selection as normal.
- The right tool gets activated only if the right mouse button (or whatever input action is assigned) is first pressed. [cc332c6](https://github.com/Orama-Interactive/Pixelorama/commit/cc332c6cbf3f9265a95a4bdc4998c9ca6c4f750a)
- No more errors in the debugger or the terminal appear when attempting to undo/redo while drawing. [af2b1fe](https://github.com/Orama-Interactive/Pixelorama/commit/af2b1feb1f63144ebce00520ea2f8ee832dc49bd)

Thank you all for taking the time to read this blog post and for supporting us. We appreciate every and each one of you, with special thanks to our contributors, our translators and our [patrons](https://www.patreon.com/OramaInteractive)! Happy painting, and keep pixelating your dreams.

Pixelorama is available on [GitHub](https://github.com/Orama-Interactive/Pixelorama) and [Itch.io](https://orama-interactive.itch.io/pixelorama)!
