---
title: "Pixelorama v0.5 is out!"
date: 2019-12-13T01:04:32+03:00
author: Emmanouil Papadeas
image: images/blog/pixelorama-0.5-is-out/main.webp
---
Major UI overhaul - at last! Artwork by Erevos

I have to say, this update was finished earlier than I expected. If you asked me some weeks ago about when v0.5 would be released, I'd say early 2020! Fortunately for all of us I was wrong, and it released just in time for something new that Orama is doing! What are we doing, you ask? I'll let you know soon, so make sure to read this blog post until the end. But for now, the changelog:

Added / changed:

- First things first, a UI overhaul! New icons for tools, tool options, new buttons in the animation timeline, a new font, better tooltips, an icon for Pixelorama and proper spacing between the UI elements! Also added tool icons that appear in the cursor! Oh and, the ugly arrows that used to be on the tools and brushes are now long gone.
- Added a new tool, the Color Picker, that lets you pick a color from the canvas.
- Removed the Paint all colors tool. It's now a part of the bucket tool instead.
- The selection tool's outline is visible only, instead of the whole blue rectangle that was on top of the selection.
- Added a mini canvas preview window. You can zoom in/out and pan.
- Rulers and guides! If you don't like seeing 'em, you can turn them off in the View menu. Guides also get saved in .pxo files.
- Pixelorama now supports multiple localisations! Well, in theory at least. For now it's only available in the English & Greek languages.
- New preferences window to change things like the language and grid size & color. More options will come in future versions.
- Removed remove/clone and move frame buttons. They now appear as menu options when you right click on a frame button instead.
- Pixelorama now remembers window settings like window size, position and if it is in fullscreen or not. To toggle fullscreen, press F11 or Alt + Enter. (Thanks to Calinou from GitHub!)
- If you open a file, its name now appears as the window title! (Again, thanks to Calinou for this)
- Left & right colors switch button, and another that resets them to their default state.
- Added hotkeys for some of the timeline's buttons.
- Added a window dialog that appears when you exit Pixelorama.
- Default FPS is now 6 instead of 1.
- File brushes now have their file name as their tooltip.

Bug fixes & performance changes:

- Although probably not an actual fix, a crash that occurred with the bucket tool has become harder to occur. Thanks to azagaya from GitHub for this, as well as everyone else who responded to the issue!
- Fixed a problem with custom brushes and alpha. Again, thanks to azagaya!
- The sprite preview that appears on the frame buttons now gets updated only on mouse release. This improves performance on large images.
- Fixed lighten/darken behavior.
- Fixed a crash that occurred when choosing "no loop" after looping with 1 frame.
- When adding a new frame, the camera now retains the zoom factor instead of setting the zoom in its default state again.
- Fixed color picker picking the blue color from the lineout of the selected pixel. Thanks to azagaya again!
- Fixed issue where Undo/Redo wasn't working when drawing using a graphics tablet.

I already thanked them numerous times, but I can't thank them enough, so thank you [Calinou](https://github.com/Calinou) and [azagaya](https://github.com/azagaya) for contributing to Pixelorama v0.5!

And here’s your showcase video!

[![Pixelorama v0.5 Showcase](https://img.youtube.com/vi/nBz0LgPx7G8/0.jpg)](https://www.youtube.com/watch?v=nBz0LgPx7G8)

But wait, there's more! Orama Interactive has launched a [public Discord server](https://discord.gg/GTMtr8s) for everyone to join, and form a wonderful community around Pixelorama, and all of Orama Interactive's projects! We would be very happy to have you on board! <3

And to prove to you that we are indeed amazing community, as we grow, we will host certain events that are usually to promote some kind of charity or fundraiser that helps improve our world. In fact, we are doing something like that right now for #TeamTrees! And the best part is, if you use Pixelorama to draw your tree and record it in video form, we will take all of your videos and put them in our YouTube channel, as a compilation video!

We can already see how excited you are, so let's not waste any more time! Join our [public Discord server](https://discord.gg/GTMtr8s) now, and start drawing! Let's unite to make this world a little better!

Also, we created a new website that will be the home of our projects. If you are interested in what we do and would like to see this website up and running for a long time, consider donating on [PayPal](https://www.paypal.com/paypalme2/OverloadedOrama) and [Ko-Fi](https://ko-fi.com/overloadedorama), or directly on itch.io! Thanks for your time and as always, happy painting! Bob Ross would be very proud with all the happy little trees you are going to make!

Pixelorama is available on [GitHub](https://github.com/Orama-Interactive/Pixelorama) and [Itch.io](https://orama-interactive.itch.io/pixelorama)!
