## Content Creation Software: Adobe Substance Painter ##

**Substance Painter** is the easiest tool of choice for creating content for **PBR.**
Instead of uploading all textures separately and adding them to your materials in-world you can now export entire materials directly from Substance Painter. These files now exist as a **Material object** in your Second Life inventory. Direct exporting from Substance to **PBR glTF** results in higher quality textures with less compression. The procedures for creating glTF files are documented below.


**New Project Template** Defaults for starting a new SL PBR project:

[Screenshot of Substance Painter New Project Template]

**Template Type** is set to ASM - PBR Metallic Roughness (Starter_Assets)

**Normal Map** remains OpenGL format

**Compute Tangent Space Per Fragment** Set to ON. Changing Normal Map and Tangent Space settings mid project will require a rebake.

**Color Management rollout** is located at the bottom of the new project window OR in a preexisting project using the **Edit> Project Configuration.**

[Screenshot of Substance Painter New Project Color Configuration Settings]


**Color Management** Choosing **Adobe ACE** in the dropdown enables additional color settings
**Import + Export Color Spaces** Use pictured specifications above. 

**Preset File** Bypass the Color Management settings by using a Preset File. Simply save the code below as a .json file and import it into your project instead. This will only set the parameters under the Color Management rollout, not your entire new project.

```
{ 
  "color settings": { 
    "working color space": "Linear sRGB IEC61966-2.1", 
    "rendering intent": "Perceptual" 
  }, 
  "bitmap import color space defaults" : { 
    "8 bit images": "sRGB IEC61966-2.1", 
    "16 bit images": "sRGB IEC61966-2.1", 
    "floating point images": "Linear sRGB IEC61966-2.1", 
    "use embedded ICC profiles when available": true 
  }, 
  "substance material": { 
    "material color space default": "Linear sRGB IEC61966-2.1" 
  }, 
  "export colors spaces" : { 
    "8 bit images": "sRGB IEC61966-2.1", 
    "16 bit images": "sRGB IEC61966-2.1", 
    "floating point images": "Linear sRGB IEC61966-2.1" 
  } 
} 

```

**Final Export Parameters** When your project is ready to export use the output template **glTF PBR Metal Roughness** in the export textures menu.

[Screenshot of Substance Painter New Project Color Configuration Settings]

**After Export** Substance Painter will export your materials with 3 additional file types in the specified folder. They are **.bin, .glb, .gltf** as well as the maps converted to **ORM** format automatically. 

