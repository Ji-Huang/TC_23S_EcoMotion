# TC_23S_EcoMotion
Project Description of EcoMotion in Tech-Challenge 23S 

Team Members: **Drishtant Sharma, Mark Hovsepyan, Ji Huang and Vasil Popgavrilov**

## Matlab Simulation

1. ...

upload files etc.

## CAD modeling

Using SOLIDWORKS or similar CAD software.

1. Overview of the model, the rotor with flux barrier is shown in white, the magnets are shown in dark gray:

![image](https://github.com/Ji-Huang/TC_23S_EcoMotion/assets/139593884/576a9362-2410-45d0-a9a3-92447d83ed37)

![image](https://github.com/Ji-Huang/TC_23S_EcoMotion/assets/139593884/1281284b-8307-45b9-86ab-82581776af43)

2. For the parameters of the CAD model, please refer to *CAD_Modeling/CAD_size.pdf*. You can also find the original SOLIDWORKS PART file and .stl files under the *CAD_Modeling* folder.

3. Tips for modeling: First draw half of the model as a stack of cylinders, and make a sketch on the side of the rotor, extrude and cut out the flux barrier. Then mirror the half model with respect to this surface to create the complete model.  Finally, project the flux barrier sketch onto another reference surface and extrude the magnet with preferably a different color.

## 3D-Printing

Using UltiMaker Cura and PLA Filament.

1. Import the prepared CAD models in STL format (.stl) to UltiMaker Cura and adjust the positioning, size and ratio.
![3d_print_image1](./3D%20Printing/images/3d_print_image1.png)

2. Place the models optimally for printing, meaning in a way that will be most stable for printing and require the least support material. Scale it to printable size.
![3d_print_image2](./3D%20Printing/images/3d_print_image2.png)

3. Adjust all the settings (e.g. resolution, infill, etc.)

    *Settings used: 
    Resolution: 0.15
    Infill: 30%, Gyroid Pattern
    Support: ON, Cross Pattern
    Adhesion: ON*
    
![3d_print_image3](./3D%20Printing/images/3d_print_image3.png)

4. Proceed and “Slice” the prepared print model, review the printing sequence, make sure that everything is going to be accomplished as intended and the print looks good. 
![3d_print_image4](./3D%20Printing/images/3d_print_image4.png)
	
5. When everything is finalized and calibrated, we can finally save the file and run it on a real 3D printer.