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


## Pytorch (e.g. CW 6-cam pipeline)
* Get a GPU job on O2: `srun -p gpu_quad -t 1:00:00 --mem 8GB --gres=gpu:1 -c 1 --pty zsh`
* Make a new env: `conda env create -n dataPy --file /path/to/dataPy_dattalab.yml`
* Install pytorch stuff: `pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117`
  * You can use `--dry-run` to test the install first if you want.
  * Cuda 11.7 is the latest Cuda 11 version that O2 supplies, and is compatible with the majority of our code. Pytorch ships their code with CUDA pre-packaged inside, so you don't need to `module load cuda` before running stuff with these pytorch packages.
 
## KPMS / Gimbal
See: https://keypoint-moseq.readthedocs.io/en/latest/install.html
I like to have two installs of KPMS and Gimbal. One set lives in my normal analysis environment, and is installed with CPU versions of JAX. The other lives in its own dedicated environment and has GPU versions of JAX. The upside of this is that you don't have multiple GPU-bound packages in your analysis directory fighting for control of different CUDAs, etc. The downside is you have two versions of KPMS and have to remember to update them both. Pick your poison!
 
