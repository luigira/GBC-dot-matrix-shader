# GBC-dot-matrix-shader
This is an interpretation of the gameboy-color-dot-matrix-white-bg slang shader from @mattakins for OpenGL graphics driver on RetroArch.

This works in any openGl handheld now!!!

I tried it on my TrimUI Smart Pro with no issues.

## Instruccions 

- Download the zip file from releases and unzip on top of the retroarch main config folder. (Make sure gbc-dot-matrix-white.glslp and shaders folder are within shaders_glsl/handheld/ )

Note: Video Scale factor on shader parameters will increase dot size for more than 3x intiger scale. 

![Imagen](https://github.com/user-attachments/assets/8582c4ea-8988-4fe6-9109-b62824e7e9d6)

## Features

- The shader only will draw a dot on colors except for white, and because the background is a mix from a paper texture and a black and white palete, it creates a really high contrast, also it has a shadow cast with a little offset for that kind of 3D effect on the dots. 

![Video](https://github.com/user-attachments/assets/5857787b-723d-4b4b-9a6c-1db9af0bbf23)

