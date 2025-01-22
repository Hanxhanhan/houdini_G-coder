# Gcoder for SideFX Houdini
**Generating .gcode program for 3D printing in Houdini by Hangchuan Wei**
## Info
The gcoder for Houdini is developed along the research project I am working on at the Bartlett School of Architecture, UCL. It's driven by the pain we have when it comes to printing the geometries in Houdini, avoids export and import between software.

Same tools can be found using rhino&grasshopper, or software like [Cura](https://ultimaker.com/software/ultimaker-cura/) and [Prusaslicer](https://www.prusa3d.com/page/prusaslicer_424/). But this time for Houdini users.

The [presentation from Prof. Diego Garcia Cuevas](https://www.youtube.com/watch?v=u4g4EYzSp38) is really helpful, check it out as well if you are a grasshopper user.

If you are interested in our work, follow [me](https://www.instagram.com/hanx_wei?) and [Beckett Lab](https://www.instagram.com/beckettlab/) in instagram.

## To use Gcoder in houdini

![image](https://github.com/user-attachments/assets/dca305f4-3ed6-4475-a69a-d5bf25f8ad6e)

0. This Gcoder sample is developed for [WASP 2040](https://www.3dwasp.com/en/ceramic-3d-printing/delta-wasp-2040clay/) and tested at B-made, you should use **your own start and end codes** for your printer. Please check workpiece dimension of your printer before use.
1. Reeplace or edit *Node: Printing_Bed* with your printing bed size in millimeter.
2. Import your geometry, edit its position, and connect to *Node: INPUT_GEO*. In the sample file, 1 unit in houdini refer to 1mm.
3. In the *Node: Controller*, give the parameters you want.

         - Layerheight (mm): the height of each layer.
         - Extrude Factor: impact the E- value in G-code, need to be tested for your printer and nozzle setup.
         - Feeding Rate-Print: The nozzle move speed in printing
         - Feeding Rate-Move: The nozzle move speed in led-in/led-out...
         - Save to: the folder save to (end with .gcode).
5. Display the *Node: Export_file*, after cook the .gcode file will be saved to the given folder.

## Printed
![b080bbffdd401ab46817df8325832eb](https://github.com/user-attachments/assets/abce32c1-19ff-4e39-b974-3c36c99f335b)
![6cecfa8d76cab73c189bde98ffe66d5](https://github.com/user-attachments/assets/0c2eddc8-2c8c-402d-baf2-473e52531552)
