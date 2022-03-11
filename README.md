# Setup

We provide two sets of instructions to install the required packages for the study group. We strongly recommend that you use Anaconda.

## Instructions for Anaconda (recommended)

Anaconda is a convenient package manager that can create isolated python environments, install python and non-python packages and libraries, and greatly simplify the process of setting up reproducible working environments. To continue with these instructions, please make sure to install Anaconda on your system.

`https://docs.anaconda.com/anaconda/install/index.html`

### 1. Clone locally

The next step is to clone or download the course material on your computer. Just run the following command where you want the material to be downloaded:

`git clone git@github.com:ThomasKealy/study-group.git`

or

`git clone https://github.com/TomKealy/study-group`

### 2. Create virtual environment

Once the material is on your computer, you'll see that the repository for this course has a file called environment.yml that includes a list of all the packages you need to install. If you run:

`cd study-group`
`conda env create -f environment.yml`

from the root course directory, it will create the environment for you and install all the packages listed. This environment can be enabled using:

`conda activate study-group`

Finally you will need to install the following packages `scikit-learn` and `statsmodels` with the following commands:

`conda install -c anaconda scikit-learn`

`conda install -c anaconda statsmodels`

### 3. Setup and launch Jupyter

Last step, make Jupyter aware of this new virtual environment. With the study-group environment activated, run:

`python -m ipykernel install --user --name study-group`

That will create what's called a kernel in Jupyter linguo (this is just a mirror of your virtual environment). Then, you can start JupyterLab to launch the coding environment:

`jupyter lab`

When you open any notebook, make sure it's using the right kernel, which will be named `study-group`.