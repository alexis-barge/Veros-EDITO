# [EDITO Hackathon Grenoble](https://github.com/edito-model-lab/2024-10_grenoble-edito-hackathon)

Veros is the VERsatile Ocean Simulator. It's a ocean model written all in python with the framework JAX. It's able to run global ocean models and also regional models. 
JAX is a framework that replace numpy to make python work on GPU with good performances and that allows automatic differentiations. 
Veros allows to chose a backend in numpy (with a CPU) and JAX (with a GPU).

## Veros as a process on EDITO platform

The objective is to offer an installed and ready-to-use minimal Veros version on the EDITO platform. 
It intends to take a Veros config file as input, and run the simulation automatically. The default case run the Veros built-in ACC config as demonstrator.

To this end, we created **Veros-demo** process on the playground section of the EDITO platform.

#### Current state

- Process is created on EDITO platform
- Execution instructions of Veros exists in a dedicated repository
- Process run the default built-in ACC config only
- Input interface exists only in appearance, given inputs won't be used to run Veros with.
- Veros outputs are not saved or transfered

#### Repository content

- **deploy/docker** : Docker material containing installation and execution of Veros
- **deploy/veros-demo** : Material to link Dockerfile on EDITO platform and create process
