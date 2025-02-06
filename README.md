# Game Boy Dot Matrix Shaders


![Image](https://github.com/user-attachments/assets/8582c4ea-8988-4fe6-9109-b62824e7e9d6)

This project is a reinterpretation of previous Game Boy and Game Boy Color shaders available for Vulkan API. This version targets diferent OpenGL versions, expecialy more modest GPU available on retro handhealds, for use with RetroArch OpenGL API.

The shaders aim to simulate a **dotted** image, mimicking the visual style of various Game Boy models, including the DMG Game Boy and a Game Boy Color. While a Dot Matrix Game Boy Color never existed, these shaders offer artistic interpretations of what such devices might have looked like, rather than direct emulations. Same can apply for the Game Boy Advance shader available in this collection. 

## Features

This collection includes seven shaders, each tailored for different Game Boy models. One of the key improvements is more efficient processing for modest hardware. The original Vulkan shader used five passes, making it very demanding on GPU resources. This updated version achieves nearly the same visual effect with only three passes, offering improved performance on a wider range of chipsets like H700, Rk3566, and other Linux based retro handheld systems.

Version 1.0.1 is compatible across several OpenGL implementations, including OpenGL Desktop (version 130), used in many entry-level handheld GPUs, as well as OpenGL ES 2.0 and 3.0 for more modern mobile devices. For high-end Android devices, the original GBC DMG shader is available with native Vulkan support. If you encounter any problems with a particular device, let me know .

# **Instructions for standalone release**  

## **Manual Installation**  

1. **Download the Shader Package**  
   - Go to the **Assets** section of the release and download **GB-Shader.7z**.  

2. **Extract the Files**  
   - Once downloaded, unzip the file. You will find a folder named **shaders_glsl**.  

3. **Copy the Folder to Your Device**  
   - You can place the **shaders_glsl** folder anywhere on your device. However, for easier access within RetroArch, it is recommended to place it in RetroArch's standard shader directory.  
 
**_NOTE: The location of this directory depends on your operating system_**

4. **Load the Shader in RetroArch**  
   - Open **RetroArch** and navigate to:  
     `Main Menu > Settings > Video > Shader Options > Load Shader Preset`  
   - Find and select the **GB-Shader** from the folder where you placed it.  

---

## **Automatic Installation (Using RetroArch’s Online Updater)**  

1. Open **RetroArch** and go to:  
   `Main Menu > Online Updater > Update GLSL Shaders`.  

2. If the **Update GLSL Shaders** option is missing, enable it by:  
   - Navigating to:  
     `Settings > User Interface > Menu Item Visibility > Show Online Updater`  
   - Set **Show Online Updater** to **ON**.  

3. Once enabled, return to the **Online Updater** and update the GLSL shaders.  

4. After updating, load the shader as described in the **Manual Installation** section.  


**Note:** The video scale factor in the shader parameters will adjust the resolution for devices with more than a 3x integer scale. If the border option is enabled, scaling should adjust automatically.

![Video](https://github.com/user-attachments/assets/5857787b-723d-4b4b-9a6c-1db9af0bbf23)
