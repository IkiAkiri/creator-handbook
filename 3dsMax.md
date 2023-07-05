## Content Creation Software: Autodesk 3DS Max 2023+ ##

**Autodesk 3ds Max (2023+)** is capable of exporting GLTF directly with a new GLTF Material node setup. 
Prior editions of 3ds max will require a different export pipeline.

**Import or create your item** Make sure you have your completed mesh in your scene.

[Screenshot of 3dsmax Material Editor Windows]

[Screenshot of 3dsmax Node Editor]


**Material Editor** Press M to access your materials. You can set up your glTF materials using either the Slate Material Editor OR the Compact Material editor.

**GLTF Setup in Slate Editor (Nodes)** In the Material Node editor, drag your textures into the viewport and plug them into the corresponding map slots in your GLTF Material. *Please refer to further 3ds max documentation if you prefer the compact material editor.*

**Apply to mesh** Apply the materials to your object in the viewport. 

**Before Export** If you are using a multi-sub material to specify your material IDs, please ensure there are no empty map slots before exporting. All textures being packed into ORM format MUST have the same dimensions and resolution to pack and export without issues. 

**Export** File>Export>Real-time Exporter will open your exporting options for glTF. Please click “Export glTF Binary (.glb)” if you’d like your materials to export separately and output a .glb file.

[Screenshot of Realtime Exporter Window]
