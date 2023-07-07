# MNIST-Playground

Training the MNIST model using PyTorch.

## Setup:

1. Creates a new Conda environment in the "base" env: `conda create --name DL-env`
2. Activate the conda environment in the "base" env: `conda activate DL-env` (base --> DL-env)
3. Install PyTorch: `conda install pytorch::pytorch torchvision torchaudio -c pytorch`
4. Install PyTorch Lightning: `pip install pytorch-lightning`
5. Install matplotlib for visualization: `pip install matplotlib`
6. Display a list of packages installed: `conda list`, or view the list in Anaconda-Navigator
7. Generate a YAML file `environment.yml` (equal to a `conda-requirements.txt`) to include packages installed by both pip and conda: `conda env export > environment.yml`. Then anyone can reproduce the environment exactly with `conda env create -f environment.yml`

## Resources:

1. [Anaconda](https://www.anaconda.com/) provides a comprehensive **_environment_** for data analysis and deep learning projects. Anaconda comes with a suite of **_pre-installed librarie_** in the "base" environment. It also includes the **_package manager_** Conda for installing additional libraries.
2. [Conda](https://docs.conda.io/en/latest/) is a cross-platform package manager.
3. Conda commands:
   - display a list of Conda commands: `conda`
   - creates a new Conda environment in the "base" env: `conda create --name ENV_NAME`
   - activate a specific conda environment in the "base" env: `conda activate ENV_NAME`
   - displays a list of all Conda envs with the active env \* labelled: `conda env list`
   - deactivate the currently **_active_** conda environment and revert back to the base environment or directly exits from the environment usage: `conda deactivate`
   - deactivate and delete an environment, plus remove all the packages installed in that env:
     ```
     conda deactivate # switched back to the base environment
     conda remove --name ENV_NAME --all
     ```
   - install a package or multiple packages into the currently active conda environment: `conda install PACKAGE_1 PACKAGE_2 PACKAGE_3`
   - display a list of packages installed: `conda list`
   - display a list of channels that Conda will search when looking for packages to install: `conda config --show channels` (a "channel" is a location where packages are stored, and it serves as the base URL of all packages)
   - add a new channel named to the top of the channel list (highest priority): `conda config --add channels CHANNEL_NAME`
   - view the existing list of channels in conda configuration, and their priority order (the channel at the top of the list has the highest priority, which will be searched first when looking for a package to install): `conda config --get channels`
4. [PyTorch](https://pytorch.org/get-started/locally/) is a machine learning framework based on the Torch library.
5. [PyTorch Lightning](https://www.pytorchlightning.ai/index.html) provides a high-level interface for PyTorch.
