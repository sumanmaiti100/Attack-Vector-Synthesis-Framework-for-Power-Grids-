# Attack-Vector-Synthesis-Framework-for-Power-Grids-

# Targeted Attack-Vector-Synthesis-Framework-for-Smart-Grids
Modern smart grids utilize advanced sensors and digital communication to manage the flow of electricity from generation source to consumption points. They also employ anomaly detection units and phasor measurement units (PMUs) for security and monitoring of grid behavior. However, as smart grids are distributed, vulnerability analysis is necessary to identify and mitigate potential security threats targeting the sensors and communication links. We propose a novel algorithm that uses measurement parameters, such as power flow or load flow, to identify the smart grid's most vulnerable operating intervals. Our methodology uses a formal tool STaliro to incorporate a Monte Carlo simulation approach to identify these intervals and deploys a deep reinforcement learning agent to generate attack vectors during the identified intervals that can compromise the grid's safety and stability in the minimum possible time, while remaining undetected by local anomaly detection units and PMUs. Our approach provides a structured methodology for effective smart grid vulnerability analysis, enabling system operators to analyze the impact of attack parameters on grid safety and stability and facilitating suitable design changes in grid topology and operational parameters.


Our framework assumes a stronger grid safety and security model by considering that 1) the generation side is equipped with anomaly based detectors sensitive to transient dynamics, 2) real time PMU measurements are available for the transmission system and 3) suitable  protection schemes exist at the generation, transmission and load side. With such security assumptions, we propose an  attack framework that simultaneously targets Automatic Generation Controlers and PMUs to maximize the physical impact of attacks on the grid in minimum possible attack duration, while remaining stealthy all the while.

<p align="center">
  <img src="https://github.com/sumanmaiti100/Attack-Vector-Synthesis-Framework-for-Smart-Grids/assets/103938112/ec0c5b80-a2b7-4f68-95c5-0711b691706b" alt="monte_carlo_intro_1" width="700">
  <br>
  <em>Figure 1: Work Flow of the Attack Vector Synthesis Framework</em>
</p>

## Prerequisites:

* Platform: 32/64 bit Windows Operating System.
* External Tools: Matlab R2021a.
* Other Requirements: S-taliro tool-box https://sites.google.com/a/asu.edu/s-taliro/s-taliro , Matlab Reinforcement Learning Toolbox.

## Installation guide:

* Setup S-taliro toolbox by pasting "setup_staliro.m" command in the Matlab command window.
* Copy all the .mat files from folder mat_files and simulink models from folder rl_models_simulink in the repository to the path C:\trunk\demos\SystemModelsAndData.

## Simulation guide:
* To find out vulnerable operating periods of a smart grid model open any slx file from the folders IEEE 14 BUS ATTACK MODEL, IEEE 37 BUS ATTACK MODEL and IEEE 39 BUS ATTACK MODEL. Next, attach goto ports on the tie lines in the models (indicated inside the model), and run the code in "MonteCarloSimulationAlgorithmCode.txt" in the maatlab command window to get the most vulnerable operating periods in the matlab workspace.
* To simulate False Data injection (FDI) attacks during the identified vulnerable operating periods, for an IEEE 14 bus model, load all the mat files in folder IEEE 14 BUS ATTACK MODEL into matlab workspace.
* Run the matlab slx file in folder IEEE 14 BUS ATTACK MODEL for desired time duration, to observe the effect of attack on the grid operating frequency through the scopes provided in the model.
* To simulate the attack in presence of protection systems in the grid, load all the mat files in the folder IEEE 14 BUS ATTACK MITIGATION into the matlab workspace and run the slx file in the same folder for the desired time duration.
* To simulate False Data injection (FDI) attacks during the identified vulnerable operating periods, for an IEEE 37 bus model, load all the mat files in folder IEEE 37 BUS ATTACK MODEL into matlab workspace.
* Run the matlab slx file in folder IEEE 37 BUS ATTACK MODEL for desired time duration, to observe the effect of attack on the grid operating frequency through the scopes provided in the model.
* To simulate the attack in presence of protection systems in the grid, load all the mat files in the folder IEEE 37 BUS ATTACK MITIGATION into the matlab workspace and run the slx file in the same folder for the desired time duration.
* To simulate False Data injection (FDI) attacks during the identified vulnerable operating periods, for an IEEE 39 bus model, load all the mat files in folder IEEE 37 BUS ATTACK MODEL into matlab workspace.
* Run the matlab slx file in folder IEEE 39 BUS ATTACK MODEL for desired time duration, to observe the effect of attack on the grid operating frequency through the scopes provided in the model.
* To simulate the attack in presence of protection systems in the grid, load all the mat files in the folder IEEE 39 BUS ATTACK MITIGATION into the matlab workspace and run the slx file in the same folder for the desired time duration.

