---
title: "Pixelorama v0.10.3 is out!"
date: 2022-09-26T17:01:26+03:00
author: Emmanouil Papadeas
image: images/blog/pixelorama-0.10.3-is-out/main.png
---
Artwork by [Kalpar](https://resite.link/Kalpar), one of the artists for v0.10's splash screen artworks.

Pixelorama v0.10.3 is out today! Unlike the versions that came before it, it does not contain a lot of new features. Nevertheless, it comes with important UI and UX improvements and polishing, as well as bug fixes, so it is highly encouraged that you update.

Pixelorama is a passion project that we work on during our free time. It is and forever will remain free for everyone, so if you wish to support us, you can [become a Patron](https://www.patreon.com/OramaInteractive) and receive exclusive awards, or [buy Pixelorama from itch.io](https://orama-interactive.itch.io/pixelorama)!

The changes that have arrived in v0.10.3 include:
### Added
- The UI now automatically gets scaled, based on the dpi and resolution of the monitor. Resolves [#643](https://github.com/Orama-Interactive/Pixelorama/issues/643).
- A "Divide into equal parts" button has been added in Gradient Map. This is meant for easy gradient bisecting, which is helpful for converting Linear/Cubic interpolated gradients into Constant. This will eventually be used in gradient generation as well, once multi-color gradient generation support gets implemented.
- A new fill area option has been added to the bucket tool options, "Whole Selection". This fills the entire selection with a color or pattern, regardless of the colors of the pixels.
- The UI can now be scaled down to 0.5 and 0.75.
- Palette swatches now get highlighted if their color is selected from the color buttons. [#730](https://github.com/Orama-Interactive/Pixelorama/pull/730)
- Project tabs can now be closed with the middle mouse button.
- Non-keyboard shortcut bindings for tools are now allowed. You can, for example, map your tools to a mouse or gamepad button.
- The background color of the canvas is now configurable, as requested in [#586](https://github.com/Orama-Interactive/Pixelorama/discussions/586).

### Changed
- Circle brushes now scale properly and support even-numbered diameters.
- Copy, cut & delete now affect the entire cel if there is no selection.
- The paste placement behavior has been changed. Paste now places the pasted content in the middle of the canvas view, instead of its original position. A new option in the Edit menu has been added, "Paste in Place", that preserves the previous behavior.
- If a layer is locked or invisible, the cursor changes into forbidden when the user is hovering the mouse over the canvas.
- The left & right tool options now have a header with the name of the currently selected tool, and a color indicator on the top.
- The preferences dialog has been polished. Headers have been added for each segment, and all of the elements are now vertically aligned with each other.
- hiDPI is now enabled - solves [#159](https://github.com/Orama-Interactive/Pixelorama/issues/159).
- The recent projects menu now makes the most recent project appear on top, and if you open a project already in the recent projects list, it would then be moved to the most recent spot on the list. [#755](https://github.com/Orama-Interactive/Pixelorama/pull/755)
- The import dialog now remembers the last option. [#754](https://github.com/Orama-Interactive/Pixelorama/pull/754)
- In the bucket tool options, "Same color area" and "Same color pixels" have been renamed to "Similar area" and "Similar colors" respectively.
- The splash and preference dialogs can now be resized to a smaller size than the default.

### Fixed
- Deleting content from locked/invisible layers is no longer possible.
- Selection can no longer be moved if there is a dialog open.
- Tool and menu shortcuts no longer get activated if a dialog is open. [#709](https://github.com/Orama-Interactive/Pixelorama/issues/709).
- Onion skinning now works properly with mirror view. Addresses part of [#717](https://github.com/Orama-Interactive/Pixelorama/issues/717).
- Fix invalid pattern image error when using the bucket tool to replace colors.
- Fixed issue with the bucket tool where if the selected color is the same as the pixel's color in mouse position, the operation stops even if there are other cels selected.
- The "Close" button in the preferences no longer remains stuck in the previous language, if the language changes and the previous one was not English.

Thank you all for taking the time to read this blog post and for supporting us. We appreciate every and each one of you, with special thanks to our contributors, our translators and our [patrons](https://www.patreon.com/OramaInteractive)! Happy painting, and keep pixelating your dreams.

Pixelorama is available on [GitHub](https://github.com/Orama-Interactive/Pixelorama) and [Itch.io](https://orama-interactive.itch.io/pixelorama)!
