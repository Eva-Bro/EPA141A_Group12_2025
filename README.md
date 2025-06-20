# Group 12 - Model-Based Decision-Making - EPA141A

This repository contains the files for the project of the course Model-Based Decision-Making (EPA141A). As group 12 our actor role is Analyst of Environmental Interest Group, and for this project we adopted the vision of the Environmental Interest Group. They are a non-profit organization who prefer Room for the River policies over dike heightening, since this is better for the environment and bio-diversity. 

The aim of this project is to find robust policies for flood risk management around the Ijssel River in the Netherlands. These policies have to match the interests of the Environmental Interest Group, as well as the interests of other actors involved. It is important that a policy is also supported by the other actors, since they have to agree to a policy before it can be implemented. 

To search for robust policies, open exploration and multi-scenario multi-objective robust decision-making (multi-scenario MORDM) have been used. These two analysis can be found in the Jupyter Notebooks with the corresponding names. 

### [Open exploration](final assignment/1_Open_Exploration.ipynb)

The open exploration is used to explore the model. Four scenarios are evaluated over 1000 scenarios. These scenarios are: 

1. Base case – No action taken, Business-As-Usual  
2. Dikes only – Increase dike heights at all locations and time steps.  
3. RfR only – Implement RfR at all locations and time steps.  
4. Final policy – Result of policy debates: combines dike increases, RfR projects, and an evacuation warning system.

A best case and worst case scenario are derived from this exploration, and these are saved to use as scenarios for the multi-scenario MORDM. 

### [Multi-scenario MORDM](final assignment/2_Multi_scenario_MORDM.ipynb)

Usually, a multi-scenario MORDM uses the results of a single scenario MORDM to create new scenarios for which the multi-scenario MORDM is performed. Due to time constraints it was decided to make an adapted multi-scenario MORDM. The scenarios in this version are based on the open exploration results instead of the outcomes of a single scenario MORDM.

The multi-scenario MORDM consists of four steps:

1. [Problem formulation](final assignment/2_Multi_scenario_MORDM.ipynb#step-1-problem-formulation)  
2. [Searching for candidate solutions](final assignment/2_Multi_scenario_MORDM.ipynb#step-2-searching-for-candidate-solutions)  
3. [Re-evaluate candidate solutions under uncertainty](final assignment/2_Multi_scenario_MORDM.ipynb#step-3-re-evaluate-candidate-solutions-under-uncertainty)  
4. [Performing a scenario discovery](final assignment/2_Multi_scenario_MORDM.ipynb#step-4-performing-a-scenario-discovery)   

The goal is to find robust policies that minimize the five outcomes of interest:

- Expected annual damage  
- Dike investment costs  
- RfR investment costs  
- Evacuation costs  
- Expected number of deaths  

During the optimization extra attention is paid to limiting the number of deaths and ensuring that at least some RfR projects are part of each policy, since these are the interests of our actor.  

### Other files

- Simulation data outputs and visualisations  
- Python files containing functions for the dike model  
- Data directory containing all data provided by the course to run the model