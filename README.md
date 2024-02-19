
# Fusion2Pybullet

Developed from [@syuntoku14/fusion2urdf](https://github.com/syuntoku14/fusion2urdf). 

### What is this script?

A Fusion 360 script to export urdf files to run simscape multibody simulations.
The install  is the same as in the original repo:

##### Windows (In PowerShell)

```powershell
cd <path to fusion2urdf>
Copy-Item ".\SimScape_Exporter\" -Destination "${env:APPDATA}\Autodesk\Autodesk Fusion 360\API\Scripts\" -Recurse
```

Notes: 
* Only tested on "Revolute" joints,  The original script supported "Rigid" and "Slider" joints but they were not tested.
* The script auto transformes the model's stl units to meters, that because 'smimport' command ignores the scaling for some reason.

This exports:

* .urdf files of the model
* .stl files of your model