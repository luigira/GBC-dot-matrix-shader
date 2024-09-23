# GBC Dot Matrix Shader

This project is a reinterpretation of the Gameboy Color Dot Matrix shader, originally developed by @mattakins for the Vulkan API and high-end devices. This version targets OpenGL drivers and more modest GPU hardware, specifically for use with RetroArch.

The shader aims to simulate a **dotted** image displayed on a white canvas, mimicking the visual style of a DMG GameBoy but with color. Since a Dot Matrix GameBoy Color never existed, this shader offers an artistic interpretation of what such a device might have looked like, rather than a direct emulation.

Version 0.9 is compatible across several OpenGL implementations, including OpenGL Desktop (version 130), used in many entry-level handheld GPUs, as well as OpenGL ES 2.0 and 3.0 for more modern mobile devices. For high-end Android devices, the original GBC DMG shader is available with native Vulkan support.

The original shader used five passes, which made it demanding on GPU resources. Most entry-level devices run with more modest GPUs and older OpenGL versions, so the challenge was to create a more efficient and less resource-intensive version.

This version achieves nearly the same visual effect with only three passes, offering improved performance on a wider range of hardware.

## Instructions

- Download the zip file from the releases page and extract it to your RetroArch configuration folder. Ensure that `gbc-dot-matrix-white.glslp` and the shader files are placed within the `shaders_glsl/handheld/` folder in your operating system.

**Note:** The video scale factor in the shader parameters will adjust the resolution for devices with more than a 3x integer scale. If the border option is enabled, scaling should adjust automatically.

![Image](https://github.com/user-attachments/assets/8582c4ea-8988-4fe6-9109-b62824e7e9d6)

## Features

- The shader will only render a dot when color information is present, except for white. Since the background is a white canvas, this creates a high-contrast image that mimics the look of a DMG GameBoy but with color. The shader also includes a subtle shadow effect with a slight offset, giving the dots a 3D appearance. This shadow, along with other visual parameters, can be adjusted through the shader settings.

![Video](https://github.com/user-attachments/assets/5857787b-723d-4b4b-9a6c-1db9af0bbf23)
