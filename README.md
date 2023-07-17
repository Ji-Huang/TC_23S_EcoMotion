# TC_23S_EcoMotion
Project Description of EcoMotion in Tech-Challenge 23S 

Team Members: **Drishtant Sharma, Mark Hovsepyan, Ji Huang and Vasil Popgavrilov**

## Matlab Simulation

Requirements: MATLAB; SyR-e (Synchronous Reluctance Evolution) which is an open source code developed in MATLAB/OCTAVE and is normally used together with FEMM (Finite Element Method Magnetics) for FEA (Finite Element Analysis) Simulations.
![5046d8d6-be65-4250-a6cc-0f70abb735a1](https://github.com/Ji-Huang/TC_23S_EcoMotion/assets/139593884/2acc7c34-1dd2-42b4-bd2f-8d5aa54762b9)

1. SyR-e consists of 2 different GUIs (Graphics User Interface) namely GUI_Syre (The main GUI) and GUI_Syre_MMM. The main GUI is mainly responsible for optimizing the design of the motor including altering the parameters of the stator, rotor as well as that of the flux barriers (Main Data Tab), inserting different types of magnetic materials in the flux barriers (Materials Tab) and carrying different type of simulations (Simulation Tab) at a particular rotor speed (usually 780 rpm)  to analyze important parameters of the motor such as the resulting torque, torque ripple and iron loss taking place in the motor . The main simulations that are carried out using this GUI are the Flux Map and Iron Loss- Flux Map Simulations. These simulations along with the drawn and evaluated slot model of the SynRM (Windings Tab) form the basis of the MMM (Magnetic Model Manipulation) Simulations further.

![7475c2f2-4b05-45f0-b339-5bd9e82360f6](https://github.com/Ji-Huang/TC_23S_EcoMotion/assets/139593884/4b90da05-d50d-4d86-a39c-fff7afcbdade)
![9d501d0b-391f-475f-a669-1bbbd62249f3](https://github.com/Ji-Huang/TC_23S_EcoMotion/assets/139593884/0a45ee8a-e960-466a-89fd-68025a9c5551)
(The Temperature Vector has been altered accordingly in order to get an appropriate Slot Model to use later for the simulation)

2. The GUI_Syre_MMM does not carry out any simulations but helps in loading the simulated data and post processing it. The Flux Map , Iron Loss - Flux Map simulation results and the Evaluated Slot Model (Skin effect Model) are loaded in that order. Then through simple manipulations various maps can be computed such as MTPA/MTPV Control Trajectories, Inductance and Anisotropy Maps, Various types of Iron Losses and Inverse Models. The most relevant ones for us, in this case, are the graphs obtained for various types of iron losses (such as Total Iron Loss and  Rotor current Eddy Loss). 

![e58cf2a6-5421-4f14-ac55-9637a13193c6](https://github.com/Ji-Huang/TC_23S_EcoMotion/assets/139593884/e8101e91-bfe7-41e9-9f5e-96e15d0c80d7)

3. The following Simulations are then first of all carried out for our prototype of the  Synchronous Reluctance Motor consisting of two pole pairs and a circular rotor (Named as TC1  in this case). 

4. Ferrite 35H Magnet , having a PM Remanence of 0.4 T is then introduced in the Flux Barriers of the Rotor of TC1 and it is turned into a Permanent Magnet assisted Synchronous Reluctance Motor (PMaSynRM)  named TC1 (Ferrite Magnet Machine) in this case using the Materials Tab of the main GUI. This Tab can be used to change the magnetic material and to alter the size and orientation of the magnet.
 
5. The same simulations are then carried out for TC1 (Ferrite Magnet Machine) and the comparison of the most important graphs is then made in order to determine how introducing the magnets helps in reducing the respective iron losses and thus making the SynRM more energy efficient. 

![54df0ad9-1057-4ba2-9bd2-7916c0bac1f9](https://github.com/Ji-Huang/TC_23S_EcoMotion/assets/139593884/c53c51ca-1e5b-4eed-8489-22572ec3e2bc)

6. The following graphs can be used to compare the Total Iron Loss and Rotor Eddy Currents of TC1 vs TC1 (Ferrite Magnet Machine) . From the above graphs it can be seen that the introduction of Ferrite Magnet has led to a 7% reduction in the Rotor Eddy current losses and a 2% reduction in the Total Iron Loss when both the motors are  simulated at a current load of 8 Amperes.

![bdd5f5db-0644-488a-841b-32a95e8d3cc1](https://github.com/Ji-Huang/TC_23S_EcoMotion/assets/139593884/bb0f5b72-4e38-4c30-aad0-1908cf38c05f)

![9e504c9d-42ad-49ce-a1a3-d285622afa4b](https://github.com/Ji-Huang/TC_23S_EcoMotion/assets/139593884/8097f61a-6e86-4d67-8aaf-cef58fbc4803)

7. These parameters can be further optimized by altering the magnetic material to be introduced in the flux barriers ( Neodymium or Strontium Magnets) and optimizing their amount and orientation to also ensure the most optimum weight to cost ratio.




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
