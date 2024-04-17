---
title: "Pixelorama v0.11.4 is out!"
date: 2024-04-17T16:00:00+02:00
author: Emmanouil Papadeas
image: images/blog/pixelorama-0.11-is-out/main.png
---
Artwork by Exuvita, one of the artists for v0.11's splash screen artworks.

Hello everyone! It's been a while since our last update. I hope you didn't miss us! Today, version 0.11.4 is coming out, along with various optimizations and bug fixes. Very few new features, but we definitely recommend you to update. Today is also Orama Interactive's birthday! It's been a wild ride, and we are very glad and honored you have been with us.

Now, you may ask yourself, why did a bug fixing update take so many months to come out? Is the project dying? The answer is no, not at all! In fact, we have been working on version 1.0, the biggest version so far, on a daily basis. A LOT of new features will arrive with 1.0, and we are also bringing Pixelorama somewhere new... I won't say where yet, but stay tuned because we will have news for you, very very soon. Until then, turn the valves of your creativity on, and blow off some steam by drawing!

As always, if you wish to support us, you can [become a Patron](https://www.patreon.com/OramaInteractive) and receive exclusive awards, or [buy Pixelorama from itch.io](https://orama-interactive.itch.io/pixelorama)!

[![Become a patron](../../images/blog/become_a_patron.png)](https://patreon.com/OramaInteractive)

What's new in v0.11.4:

### Added
- Exporting palettes to png files is now possible.
- Progressive Web App (PWA) has been enabled for the Web version.

### Changed
- When quitting, multiple save confirmation dialogs now appear, each for every project that has changes.
- Loop through frames when clicking on go to previous/next frame buttons on the timeline.
- High res display is now enabled on macOS. [#936](https://github.com/Orama-Interactive/Pixelorama/issues/936)
- Make cloned frames only select a cel if its corresponding original cel was selected as well. [#941](https://github.com/Orama-Interactive/Pixelorama/pull/941)
- All of the timeline buttons now have the same size (24x24).

### Fixed
- Memory usage has been greatly optimized when doing operations such as drawing, image effects, selecting, transforming, etc, as the images stored in memory are now compressed. [#883](https://github.com/Orama-Interactive/Pixelorama/issues/883)
- Fixed memory leak when applying image effects. [7235617db7c21837edc7ba7b95f2e7eeb1140691](https://github.com/Orama-Interactive/Pixelorama/commit/7235617db7c21837edc7ba7b95f2e7eeb1140691)
- Fixed memory leak when previewing layouts in the Manage Layouts dialog. [b2f511c45be61cd26f01e134bf7a6a55109f46ad](https://github.com/Orama-Interactive/Pixelorama/commit/b2f511c45be61cd26f01e134bf7a6a55109f46ad)
- Attempting to load an invalid pxo file no longer crashes the application. [3f6e1385e06cd7801fe12fbf90a9649557ea8f2e](https://github.com/Orama-Interactive/Pixelorama/commit/3f6e1385e06cd7801fe12fbf90a9649557ea8f2e)
- Tool shortcuts can now work with <kbd>Control</kbd>. [#935](https://github.com/Orama-Interactive/Pixelorama/issues/935)
- Optimize canvas drawing by only updating it when the image(s) have changed. [ac6a4db43d9296ebc03e639d8199dd3878a25d86](https://github.com/Orama-Interactive/Pixelorama/commit/ac6a4db43d9296ebc03e639d8199dd3878a25d86)
- Fix bug where using shortcuts to switch between frames also moved the selection, causing deletions.
- Pxo files can now be loaded from the Open menu option in the Web version. [3dcc51705a999145e53a8e6d4de217dc03b0f147](https://github.com/Orama-Interactive/Pixelorama/commit/3dcc51705a999145e53a8e6d4de217dc03b0f147)
- The same frames are no longer being exported multiple times when "Selected frames" is selected, and multiple cels of the same frames are currently selected on the timeline. [#1001](https://github.com/Orama-Interactive/Pixelorama/issues/1001)
- Fixed crash due to division by zero when locking two or three ValueSliders, and one of them has the value of 0 and the user attempts to change it. [3b8c63c4a6a3325707ef624942ea50834634e45c](https://github.com/Orama-Interactive/Pixelorama/commit/3b8c63c4a6a3325707ef624942ea50834634e45c)
- Fixed exporting selected layers not including the non-selected frames. [324e21776de853e6ea24703d5724a491547371ab](https://github.com/Orama-Interactive/Pixelorama/commit/324e21776de853e6ea24703d5724a491547371ab)
- Fix bug where images with width or height 1 are being completely cleared by image effects. [fcfc606861d247856db5473b702628ebd71df43f](https://github.com/Orama-Interactive/Pixelorama/commit/fcfc606861d247856db5473b702628ebd71df43f)
- Made the color picker not select fully transparent pixels that are not black. [#999](https://github.com/Orama-Interactive/Pixelorama/issues/999)
- Brushes are no longer being drawn outside the selection, if the selection is outside the canvas. [5f43a3e2829a7119d18d0762796222f20170f410](https://github.com/Orama-Interactive/Pixelorama/commit/5f43a3e2829a7119d18d0762796222f20170f410)
- Bucket "similar color" and "whole selection" modes and image effects no longer affect pixels outside the selection area, if the selection is outside the canvas. [436406a527f0db67c5e2b58a90b43597b3168600](https://github.com/Orama-Interactive/Pixelorama/commit/436406a527f0db67c5e2b58a90b43597b3168600)
- The ellipse tool no longer produces gaps with large sizes. [4f3a7a305a264e0d2fe86c201af76eca4b2fea0a](https://github.com/Orama-Interactive/Pixelorama/commit/4f3a7a305a264e0d2fe86c201af76eca4b2fea0a)
- Fix "visible layers" option on the export dialog producing wrong results. [346d1f071a8c6b1defb1072d39aea9c642f1ef59](https://github.com/Orama-Interactive/Pixelorama/commit/346d1f071a8c6b1defb1072d39aea9c642f1ef59)
- Random brushes now work again. [1317e40ffa5e9f01a9d214221bb5133db20a1de9](https://github.com/Orama-Interactive/Pixelorama/commit/1317e40ffa5e9f01a9d214221bb5133db20a1de9)
- Fixed issue where the override.cfg file would be created at the wrong location, if Pixelorama is launched through a shortcut. [0c6566de761a683a0e8a781131024a1dedb9734f](https://github.com/Orama-Interactive/Pixelorama/commit/0c6566de761a683a0e8a781131024a1dedb9734f)
- The gizmo in the rotation image effect dialog is now accurately following the mouse.
- Fixed the size label not being updated on the Export dialog's spritesheet tab when the direction changes. [9a5eb9720d2328f914f8efc3b9aa605dadca99b0](https://github.com/Orama-Interactive/Pixelorama/commit/9a5eb9720d2328f914f8efc3b9aa605dadca99b0)
- The "Export dimensions" label in the export dialog no longer shows fractions as the final image's size.

Thank you all for taking the time to read this blog post and for supporting us. We appreciate every and each one of you, with special thanks to our contributors, our translators and our [patrons](https://www.patreon.com/OramaInteractive)! Happy painting, and keep pixelating your dreams.

Pixelorama is available on [GitHub](https://github.com/Orama-Interactive/Pixelorama) and [Itch.io](https://orama-interactive.itch.io/pixelorama)!
