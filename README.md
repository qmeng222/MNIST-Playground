# MNIST-Playground

Training the MNIST model using PyTorch.

## Setup:

1. Creates a new Conda environment in the "base" env: `conda create --name DL-env`
2. Activate the conda environment in the "base" env: `conda activate DL-env` (base --> DL-env)
3. Install PyTorch: `conda install pytorch::pytorch torchvision torchaudio -c pytorch`
4. Install PyTorch Lightning: `pip install pytorch-lightning`
5. Install matplotlib for visualization: `pip install matplotlib`
6. Display a list of packages installed: `conda list`, or view the list in Anaconda-Navigator
7. Generate a YAML file `environment.yml` (equal to a `conda-requirements.txt`) that contains a list of all packages installed by both pip and conda in the current conda env: `conda env export > environment.yml`. Then anyone can reproduce the environment exactly with `conda env create -f environment.yml`

## Study notes:

1. There're different modes when opening a file in Python:
   - "Read" mode: Getting data from the file, not putting data into the file.
   - "Write" mode: When a file is opened in write mode, the file is created if it does not exist. If it does exist, the "write" mode starts fresh and overwrites the existing content of the file. Your program is ready to write data to this file.
   - "Binary" mode: Most files that we encounter are text files where the data is in human-readable format. But when dealing with non-text files like images, audio, or video files, the data should be handled in binary mode, where the data is stored in binary format (a sequence of bytes). When you open a file in binary mode, you are telling Python to handle the file in a format suitable for non-text data.
2. The `.as_posix()` method in Python's `pathlib` module returns a string representation of the path with forward slashes (/):
   ```python
   from pathlib import Path
   p = Path('a/b/c')
   print(p.as_posix())  # Output: 'a/b/c'
   ```
3. `(x_train, y_train), (x_valid, y_valid), _` is an example of tuple unpacking in Python:
   - `(x_train, y_train)` represents the first item returned (a tuple of two items). `x_train` represent the training data or features, and `y_train` represent the corresponding labels
   - `(x_valid, y_valid)` similarly represents the second item returned. `x_valid` is the validation data or features, and `y_valid` is the validation labels.
   - `_` (an underscore) is a common convention in Python for a "throwaway" variable, a variable that you don't plan to use. In this case, the underscore represents the third item returned by the function. By assigning this value to `_`, your code is effectively saying "there's a third item returned by this function, but we don't care about it and aren't going to use it."
4. fdf

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
     ```python
     conda deactivate # switched back to the base environment
     conda remove --name ENV_NAME --all
     ```
   - install a package or multiple packages into the currently active conda environment: `conda install PACKAGE_1 PACKAGE_2 PACKAGE_3`
   - display a list of packages installed: `conda list`
   - display a list of channels that Conda will search when looking for packages to install: `conda config --show channels` (a "channel" is a location where packages are stored, and it serves as the base URL of all packages)
   - add a new channel named to the top of the channel list (highest priority): `conda config --add channels CHANNEL_NAME`
   - view the existing list of channels in conda configuration, and their priority order (the channel at the top of the list has the highest priority, which will be searched first when looking for a package to install): `conda config --get channels`
4. [PyTorch](https://pytorch.org/tutorials/) is a machine learning framework based on the Torch library
5. [WHat is torch.nn really?](https://pytorch.org/tutorials/beginner/nn_tutorial.html)
6. [PyTorch Lightning](https://www.pytorchlightning.ai/index.html) provides a high-level interface for PyTorch
7. [pathlib](https://docs.python.org/3/library/pathlib.html) | object-oriented filesystem paths
8.
