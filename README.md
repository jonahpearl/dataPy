# dataPy
A generic conda virtual environment template for data science. Conda can create virtual envs from yml templates!

To use:
* clone the repo, or just download the yaml file to a convenient location.
* If you haven't already, install anaconda or miniconda (https://docs.anaconda.com/anaconda/install/). Ensure that when you open a new terminal window, the base environment is activated (as shown by "(base)" before the terminal prompt). If not, try `conda init` (or `conda init zsh` if you're using zsh, or `conda init bash`, or...). If that, too, fails, you probably didn't install conda correctly.
* If you need a specific version of Python (e.g. as specified by a major package like CaImAn or DeepLabCut or etc), change the corresponding line in the yaml file.
* run: `conda env create -n dataPy --file /path/to/dataPy_packages.yml`
* Then, for example:
* `conda activate dataPy`
* `jupyter notebook`
