---
title: Temporal Anti-Aliasing
publishDate: 2026-05-27 15:00:00
img: /assets/TAAScreenshot.png
img_alt: A frame treated with TAA
description: |
  A deferred Vulkan renderer created from scratch featuring both FXAA and TAA
tags:
  - Unity
  - C#
  - FPS
---
## An investigation into Vulkan and Temporal Anti-Aliasing
### Links:
<iframe width="600" height="400" src="https://www.youtube.com/embed/cKglwx3UG-A" title="Vulkan TAA demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> <br>
Repository including original project files: <br> 
<a href="https://github.com/puffledude/JDEngine">Github Project Link</a>

### What I did
For my final masters project, I decided to investigate Temporal Anti-Aliasing (TAA). The standard anti-aliasing technique for most modern AAA video games, TAA involves blending the current frame with colours sampled from the previous. Whilst effective, TAA can harm images with artifacts such as flicker, blur and ghosting. <br>
By implementing my own TAA shader it was possible to investigate how these issues manifest and how they can be mitigated. A new renderer created from scratch using Vulkan was implemented to fulfill this. It felt important to use Vulkan because it is one of the main currently supported rendering APIS is use throughout industry.
### What I learned
Temporal Anti-Aliasing can significantly improve a games visual output. Both TAA and FXAA effectively treated the edges of geometry. TAA however, significantly improved the output of screenspace effects over FXAA. Issues such as ghosting and blur were able to significantly reduced with the implementation of neighbourhood clamping. Not all artifacts however, were able to be mitigated. Shadows flicker up close and textures do noticeably smear on fast camera movement. These were not issues with FXAA due to its simple nature and lack of reprojection, resulting in a more temporarily stable image.
### Future work
The renderer and engine created to show off the TAA implementation don't show the advantages of TAA as well as it should compared to FXAA. Work to be done in future should strive to do so. Techniques such as global illumination and particles would likely do so. Furthermore, the TAA could also be utilised to add upscaling for those with weaker hardware.