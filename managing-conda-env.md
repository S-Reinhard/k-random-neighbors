# Managing the conda-env of this Project

The `ml-env-config.yml` is a back up of a working virtual environment for this project.
To activate the environment in your terminal use `conda activate ml-env` python will then be able to use all packages installed within the virtual environment.

## Creating the env-from file
Open the terminal in the root of this Project and use the command `conda env create --file ml-env-config.yml` to create a conda environment named ml-env and automaticly install all required packages.

## Updating the ml-env-config.yml
If the environment ml-env already exists on your device, and you want to apply changes that are provided by the ml-env-config.yml use the commands:
`conda activate ml-env`
`conda env update --file .\ml-env-config.yml --prune`

## Removing the ml-env environment
If you want to delete the environment just do:
`conda activate ml-env`
`conda remove --name ml-env --all`