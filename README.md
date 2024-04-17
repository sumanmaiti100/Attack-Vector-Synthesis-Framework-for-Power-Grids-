# Attack-Vector-Synthesis-Framework-for-Power-Grids-

Modern smart grids utilize advanced sensors and digital communication to manage the flow of electricity from generation source to consumption points. They also employ anomaly detection units and phasor measurement units (PMUs) for security and monitoring of grid behavior. However, as smart grids are distributed, vulnerability analysis is necessary to identify and mitigate potential security threats targeting the sensors and communication links. We propose a novel algorithm that uses measurement parameters, such as power flow or load flow, to identify the smart grid's most vulnerable operating intervals. Our methodology uses a formal tool STaliro to incorporate a Monte Carlo simulation approach to identify these intervals and deploys a deep reinforcement learning agent to generate attack vectors during the identified intervals that can compromise the grid's safety and stability in the minimum possible time, while remaining undetected by local anomaly detection units and PMUs. Our approach provides a structured methodology for effective smart grid vulnerability analysis, enabling system operators to analyze the impact of attack parameters on grid safety and stability and facilitating suitable design changes in grid topology and operational parameters.


Our framework assumes a stronger grid safety and security model by considering that 1) the generation side is equipped with anomaly based detectors sensitive to transient dynamics, 2) real time PMU measurements are available for the transmission system and 3) suitable  protection schemes exist at the generation, transmission and load side. With such security assumptions, we propose an  attack framework that simultaneously targets Automatic Generation Controlers and PMUs to maximize the physical impact of attacks on the grid in minimum possible attack duration, while remaining stealthy all the while.


## Prerequisites:

* Platform: 32/64 bit Windows Operating System.
* External Tools: Matlab R2021a or higher version with support for Reinforcement Learning toolbox enabled


## Simulation guide:
* To simulate False Data injection (FDI) attacks generated by the RL agent, for an IEEE 14 bus model, load all the mat files in folder IEEE 14 BUS ATTACK MODEL into matlab workspace.
* Run the matlab slx file in folder IEEE 14 BUS ATTACK MODEL for desired time duration, to observe the effect of attack on the grid operating frequency through the scopes provided in the model.
