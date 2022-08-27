# dataPy
A generic conda virtual environment template for data science. Conda can create virtual envs from yml templates!

To use:
* clone the repo, or just download the yaml file to a convenient location.
* install anaconda or miniconda (https://docs.anaconda.com/anaconda/install/). Ensure that when you open a new terminal window, the base environment is activated (as shown by "(base)" before the terminal prompt). If not, try `conda init`. If that, too, fails, you probably didn't install conda correctly.
* run: `conda env create -n dataPy --file /path/to/dataPy_packages.yml`
* Then, for example:
* `conda activate dataPy`
* `jupyter notebook`
