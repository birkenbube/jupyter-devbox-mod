# jupyter-devbox

A Docker development box for Jupyter Notebook's with a focus on Computer Vision, Machine Learning, Statistics and Visualization.

#### What is this?

This is a Docker container based on Debian Linux (see [Dockerfile](https://github.com/jakoch/jupyter-devbox/blob/main/.devcontainer/Dockerfile)).
It sets up a Python/Jupyter Notebook development environment for Visual Studio Code.
The pre-installed libraries include OpenCV, Tensorflow, Keras, Numpy, Pandas, Sklearn, Scipy, Matplotlib, Seaborn, Imutils, SqlAlchemy.

#### What is pre-installed?

Base: Debian 10 - Buster

On top of the base image the following tools are installed:
- zsh, git, cmake
- curl, wget
- imagemagick, gnuplot, graphviz

These programming languages are included:
 - Python 2 & 3 (including wheel, setuptools, pip)
 - C & C++ (g++)

The installed Python libraries are:
 - jupyter ipykernel docutils pyyaml pylint h5py
 - tensorflow keras
 - numpy pandas sklearn scipy
 - matplotlib seaborn
 - opencv-python
 - imutils
 - sqlalchemy
 - pyautogui

#### Prerequisites

You need the following things to run this:

- Docker
- Visual Studio Code

#### How to run this?

1. Get the source: clone this repository using git or download the zip
2. Open the source folder in VSCode as a workspace (`File > Open Workspace`)
3. Then reopen the workspace inside the container (`Remote Containers: Reopen in Container`):

   This will build the container image (`Starting Dev Container (show log): Building image..`)

   Which takes a while...

   Then, finally...

4. Open the file `notebooks\test.ipynb`
5. You might get a warning message for "untrusted" Notebook content.

   Click `Trust` to allow executing the content of the Notebook.

6. Enjoy! :sunglasses:
