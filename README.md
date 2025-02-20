# dimelo_v2_image

This repository builds a DiMeLo_v2 enabled Apptainer image.

The image will contain [the dimelo_v2 Python package](https://github.com/streetslab/dimelo_v2) as well as the latest version of [modkit](https://github.com/nanoporetech/modkit) installed from the github repo.

The main interface to this image is a Jupyter Lab notebook server.
How this image can be used is described in detail in my [Apptainer HOWTO](https://github.com/stela2502/Singularity_Tutorial).

# Install

```
git clone https://github.com/stela2502/dimelo_v2_image.git
cd dimelo_v2_image
make restart build
```

Will build a sandbox folder 'dimelo' and an Apptainer image "dimelo_v1.0.sif"

The deploy target of the Makefile will create a Slurm Lua Module that we use to load the image on the Lunarc COSMOS-Sens HPC system.

You can modify the Makefiles deploy target to your needs and then call

```
make deploy
```
To install the image to this location.


# Start Up

```
apptainer run dimelo_v1.0.sif
```

