---
title: "Announcing Voxelorama"
date: 2022-06-06T16:02:03+03:00
author: Emmanouil Papadeas
image: images/blog/announcing-voxelorama/voxelcraft.png
---
Art by [Erevoid](https://www.instagram.com/erevoid/).

In our previous blog post about Pixelorama v0.10, we teased about an exciting announcement for our 10 years of Orama Interactive anniversary (17 of April 2012- 17 of April 2022). Two months ago we made a peculiar April Fools prank on our Discord server. We announced a Pixelorama extension that converts 2d pixels into 3d voxels, called Voxelorama, and that it would cost $9.99. But the next day, we admitted that this was, in fact, just a prank. Voxelorama will be **free and open-source**. Got you real good! So yes, Voxelorama is indeed a thing and it will be free. Notice the usage of future tense, but more on that later. Keep on reading to learn how you can get access to Voxelorama right now!

So, what is Voxelorama exactly and what does it do? Here is a feature list of its current capabilities.
- Convert your pixel art into voxel art. Each pixel is converted to one voxel of the same color.
- Export the generated models as .obj files, with more file types planned for the future.
- Each layer has a different depth.
- A depth tool that lets you set the depth value for each individual pixel that will be converted into a voxel. Pixels with larger depth values will be converted to voxels with more depth than those with smaller depth values.
- No color and size restrictions. However, keep in mind that the model generation and file export will be considerably slow for large images.
- A "merge frames" option that merges the cels of all frames into one. This is useful for drawing different parts of each layer in different places, and during mesh generation have them automatically merge.
- Optimized mesh generation. To reduce the amount of triangles, neighboring cubes are combined into a single 3D rectangle. So for example, a 64x64 filled image will be converted into one big cube instead of smaller 64x64 cubes.
- The UV texture is essentially the sprite itself, and each layer has a different UV texture. In the future we could allow for more traditional UV texture options as well.

So, what is its status? While Voxelorama is in fact real, it is not a high priority project at the moment. **Pixelorama itself and game development are our highest priorities**. Meaning, Voxelorama is not being worked on very actively, and it is still very early in development, which is the reason why we haven't released it yet. While we could release it since it is functional, it is not polished, unoptimized, still lacks some features and in general it is not in a state we feel confident to release it for public usage. On the other hand, it is a shame for it to be sitting there unused and not given much attention.

For this reason, we are announcing **Voxelorama Early Access**. Patrons of membership level of **Dreamers** ($10) and above, will get access to Voxelorama as it is right now, and as we keep developing it. This is also a great way for you to fund Voxelorama's development, and allow us to develop it faster. Basically, the more patrons support us, the faster Voxelorama will be developed and released to the public! To show our gratitude towards all of the amazing people that have helped with the development of Pixelorama, we will also extend access to the contributors as well. If you are eligible for Voxelorama Early Access, join our [Discord server](https://discord.gg/GTMtr8s) and look for the #voxelorama channel.

Some of the improvements we'd like to make are:
- Finalize Pixelorama's extension system to ensure backwards compatibility and keep the extension codebase steady.
- Polish the UI. Right now it looks very basic and more like a prototype than a final product. We're also not sure if it's a good idea to have Voxelorama as a popup window, or a part of the main UI. This is where your feedback comes in! :)
- Add more export file types, such as .gltf and .svg.
- Make the depth tool more powerful to use, by adding lines and fill options.
- Optimize the generated mesh even further to remove triangles on the sides of the 3D rectangles that are not visible and thus, not needed.
- Improve performance of Voxelorama on large images. We may need to use GDNative (or GDExtension if we move to Godot 4.0) to achieve greater mesh generation and export speeds. Multi-threading is also a good idea to prevent the entire app from hanging while generating/exporting.
- Give users the options to select optimization level and the UV texture type.

The below ideas are not needed for Voxelorama to exit early access and probably will not happen in the near future, but we may be able to implement with enough funding.
- Let users draw each side of the mesh.
- Add a shape tool that lets users draw with non-square shapes. This will allow multiple types of shapes besides cubes to be used for voxel art.
- The ability to draw voxels directly in a 3D environment, which can also be converted back to 2D. It would basically be the reverse process of what it does now.

Thank you all for taking the time to read this blog post and for supporting us. We appreciate every and each one of you, but we'd like to give special thanks to our contributors, our translators and our patrons! If you wish to support us, you can [become a Patron](https://www.patreon.com/OramaInteractive) and receive exclusive awards, or [buy Pixelorama from itch.io](https://orama-interactive.itch.io/pixelorama)! Happy painting, and keep pixelating (and voxelating?) your dreams.

Pixelorama is available on [GitHub](https://github.com/Orama-Interactive/Pixelorama) and [Itch.io](https://orama-interactive.itch.io/pixelorama)!
