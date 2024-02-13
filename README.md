# jupyter-devbox [![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/jakoch/jupyter-devbox/release.yml?branch=main&style=flat&logo=github&label=Image%20published%20on%20GHCR)](https://github.com/jakoch/jupyter-devbox)

A Docker development box for [Jupyter Notebooks][jupyter_website] with a focus on Computer Vision, Machine Learning, Statistics and Visualization.

#### What is this?

This is a Docker container supporting multiple architectures ([amd64][amd64_dockerfile] & [arm64][arm64_dockerfile]) based on Debian Linux.
It sets up an Jupyter Notebook development environment for interactive Python programming for [Visual Studio Code](vscode_website).
The pre-installed libraries include OpenCV, Tensorflow, Keras, Numpy, Pandas, DuckDB, Sklearn, Scipy, Matplotlib, Seaborn, Imutils, SqlAlchemy.

#### What is pre-installed?

Base: Debian 12 - Bookworm

On top of the base image the following tools are installed:
  - zsh, git, cmake, nano
  - curl, wget
  - imagemagick, gnuplot, graphviz

These programming languages are included:
  - Python 3 (including  pip, setuptools, wheel, venv)
  - C & C++ (g++)

The installed Python libraries are:
  - jupyter ipykernel docutils pyyaml pylint
  - h5py
  - tensorflow keras
  - pandas pandas-datareader
  - duckdb
  - numpy scipy sklearn
  - matplotlib seaborn plotly graphviz
  - opencv-python-headless
  - imutils
  - sqlalchemy
  - pyautogui
  - yfinance alpha_vantage nasdaq-data-link
  - financetoolkit financedatabase
  - statsmodels
  - requests_cache

You can find the list of all installed packages in the [notebooks/check_devbox.ipynb][check_devbox_ipynb_main] Notebook.

#### Prerequisites

You need the following things to run this:

- Docker
- Visual Studio Code

#### How to run this?

There are two ways of setting the container up.

Either by building the container image locally or by fetching the prebuild container image from the Github container registry.

##### Building the Container Image locally using VSCode

- **Step 1.** Get the source: clone this repository using git or download the zip

- **Step 2.** In VSCode open the folder in a container (`Remote Containers: Open Folder in Container`):

  This will build the container image (`Starting Dev Container (show log): Building image..`)

  Which takes a while...

  Then, finally...

- **Step 3.** Open the file `notebooks\test.ipynb`
- **Step 4.** You might get a warning message for "untrusted" Notebook content.

  Click `Trust` to allow executing the content of the Notebook.

- **Step 6.** You are now able to edit cells and run their content interactively.

  You might also run your scripts inside your browser at http://localhost:8888/

  And you can also read and run your scripts via the Github website: [notebooks/test.ipynb][test_ipynb_main].

-   **Step 6.** Enjoy! :sunglasses:

##### Fetching the prebuild container image

This container image is published to the Github Container Registry (GHCR).

You may find the package here: https://github.com/jakoch/jupyter-devbox/pkgs/container/jupyter-devbox.

You can install the container image from the command line:
```
docker pull ghcr.io/jakoch/jupyter-devbox:latest
```

You might also use this container image as a base image in your own Dockerfile:
```
FROM ghcr.io/jakoch/jupyter-devbox:latest
```

[jupyter_website]:https://jupyter.org/
[vscode_website]:https://code.visualstudio.com/
[test_ipynb_main]:https://github.com/jakoch/jupyter-devbox/blob/main/notebooks/test.ipynb
[check_devbox_ipynb_main]:https://github.com/jakoch/jupyter-devbox/blob/main/notebooks/check_devbox.ipynb
[amd64_dockerfile]:https://github.com/jakoch/jupyter-devbox/blob/main/.devcontainer/amd64/Dockerfile
[arm64_dockerfile]:https://github.com/jakoch/jupyter-devbox/blob/main/.devcontainer/arm64/Dockerfile
