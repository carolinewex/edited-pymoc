# edited-pymoc
This is an edited version of the NadeauJansen two-basin multicolumn model of the ocean's meridional 
overturning circulation (MOC), created using PyMOC modules that solve for 1D advection-diffusion 
equations with given isopycnal transports using diagnotic relationships, wind- and eddy-driven 
residual circulation in a Southern Ocean channel, and geostrophic exchange between regions. 
You can find this updated model in the TwoBasinUpdated_NadeauJansen.py file. More details on 
the original PyMOC modules and two basin model (titled twobasin_NadeauJansen.py in the PyMOC repository) 
can be accessed here: https://pymoc.github.io. A linear equation replaces the southern ocean surface 
buoyancy, as well as an additional save_iters variable to save the output of the simulation 
at specific time intervals. The save_iters is added into the time stepping loop and is partially 
based off of the run_JansenNadeau_2018.py example in the PyMOC repository. 

We prescribed a constant surface buoyancy increase of 0.002, 
0.004, and 0.006 to the boundary conditions. These npz.files are located in the 
surfaceb-inc-simulation folder. These warming simulations are loosely based off of 
2k, 4k, and 6k warming simulations in an MITgcm ocean-ice model. More of the  
GCM model can be found here: https://mitgcm.readthedocs.io. The output of these 
simulations can be plotted in the ReadInPlot_NadeauJansen.ipynb, 
along with the updated initial conditions which are located in the main branch. 
The ReadInPlot jupyter notebook was created based off of the Plot_overturning.py example 
in the PyMOC repository. Here, we are able to plot the streamfunctions and buoyancies
of each region as a function of depth and time, or we can look at the profiles of each variable
either over the entire simulation, or a single timestep. 
