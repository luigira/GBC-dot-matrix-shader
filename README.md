# Game Boy Dot Matrix Shaders


![Image](https://github.com/user-attachments/assets/8582c4ea-8988-4fe6-9109-b62824e7e9d6)

This project is a reinterpretation of previous Game Boy and Game Boy Color shaders available for Vulkan API. This version targets diferent OpenGL versions, expecialy more modest GPU available on retro handhealds, for use with RetroArch OpenGL API.

The shaders aim to simulate a **dotted** image, mimicking the visual style of various Game Boy models, including the DMG Game Boy and a Game Boy Color. While a Dot Matrix Game Boy Color never existed, these shaders offer artistic interpretations of what such devices might have looked like, rather than direct emulations. Same can apply for the Game Boy Advance shader available in this collection. 

## Features

This collection includes seven shaders, each tailored for different Game Boy models. One of the key improvements is more efficient processing for modest hardware. The original Vulkan shader used five passes, making it very demanding on GPU resources. This updated version achieves nearly the same visual effect with only three passes, offering improved performance on a wider range of chipsets like H700, Rk3566, and other Linux based retro handheld systems.

Version 0.9.1 is compatible across several OpenGL implementations, including OpenGL Desktop (version 130), used in many entry-level handheld GPUs, as well as OpenGL ES 2.0 and 3.0 for more modern mobile devices. For high-end Android devices, the original GBC DMG shader is available with native Vulkan support.

## Instructions

1. Download the zip file from the releases page and extract it to your RetroArch configuration folder. Ensure that the shader files are placed within the `shaders_glsl/handheld/` folder in your operating system.
2. Make sure `gbc-dot-matrix-white.glslp` is included in the extracted files.

Also this shaders are available through RetroArch native online updater, just update your shaders from menu and you good to go. 

**Note:** The video scale factor in the shader parameters will adjust the resolution for devices with more than a 3x integer scale. If the border option is enabled, scaling should adjust automatically.

![Video](https://github.com/user-attachments/assets/5857787b-723d-4b4b-9a6c-1db9af0bbf23)
