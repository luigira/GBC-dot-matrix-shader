# Game Boy Dot Matrix Shaders

![image](https://github.com/user-attachments/assets/e99769e9-1646-4a5c-9a6b-913f295a3823)

This project is a reinterpretation/translation/new aproach of several previous Game Boy, Game Boy Color, and Game Boy Advance shaders available for more modern Vulkan APIs, designed for more powerful hardware like Android devices and desktop computers. This version targets different OpenGL devices, especially more modest ones with GPUs capable of older OpenGL APIs and ES editions, mostly found in retro handhelds (small Linux-based PCs), for use primarily within RetroArch and the OpenGL video driver.

The shaders aim to simulate a **dotted image**, mimicking the visual style of origignal DMG Game Boy model. While a Dot Matrix Game Boy Color never existed, these shaders offer an artistic interpretations of what such devices might have looked like, rather than direct emulations. Same can apply for the Game Boy Advance shader available in this collection. 

## Features
![image](https://github.com/user-attachments/assets/66fe350a-8217-457e-ac5f-3c61fb224805)

This collection includes seven shaders, each tailored for different Game Boy models. One of the key improvements is more efficient processing for modest hardware. The original Vulkan shader used five passes, making it very demanding on GPU resources. This updated version achieves nearly the same visual effect with only three passes, offering improved performance on a wider range of chipsets like H700, Rk3566, and other Linux based retro handheld systems.

Version 1.0.1 is compatible across several OpenGL implementations, including OpenGL Desktop (version 130), used in many entry-level handheld GPUs, as well as OpenGL ES 2.0 and 3.0 for more modern mobile devices. For high-end Android devices, the original GBC DMG shader is available with native Vulkan support. If you encounter any problems with a particular device, let me know .

![image](https://github.com/user-attachments/assets/24bd549b-6bff-4076-abef-0e0b00a759e2)

The original DMG, Pocket, and Light Game Boys aim to replicate the screen appearance of their respective devices. In contrast, the GBC and GBA dot-matrix simulations are both artistic interpretations and aspirations. My most played games are RPGs with substantial text (aka Final Fantas* and monster-catching games like Pok*mon). Therefore, I desire a shader that doesn't apply dots to the white spaces, akin to the DMG approach. I can't recall if the DMG truly had this feature, but I aim to emulate a dot-matrix screen where only black dots appear where information is displayed; in the case of the GBC and GBA, in color. This way, white spaces remain white, while colored areas exhibit a simulated dot-matrix effect.

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
