# Anaconda and Jupyter Lab Environment Setup

## Setup Anaconda Virtual Environment 

### 1. Create a Virtual Environment:

To create a new virtual environment

```bash
conda create --name your_environment_name python=3.x
```

Example:

```bash
conda create --name study-machine-learning python=3.11
```

### 2. Activate the Virtual Environment:

- On macOS/Linux:

```bash
source activate study-machine-learning
```

### 3. Verify Activation:

You should see the environment name in your command prompt or terminal prompt, indicating that the virtual environment is active.

### 4. Install Packages:

Now, you can use `conda install` to install packages within this virtual environment. For example:

```bash
conda install numpy pandas scikit-learn
```

### 5. Run Jupyter Lab

```bash
jupyter lab
```

### 6. Deactivate the Virtual Environment:

When you're done working in the virtual environment, you can deactivate it using:

```bash
conda deactivate
```

### Note:

- Remember to activate your virtual environment every time you want to work within it.
- You can check your installed packages and environment details with `conda list` while the virtual environment is active.

By creating and using virtual environments, you can isolate your project dependencies and avoid conflicts with other projects. It's a good practice for managing dependencies in Python projects.

## Setup Jupyter Lab Server Configuration

docs : https://jupyter-server.readthedocs.io/en/latest/users/configuration.html

### 1. Generate config `/.jupyter/jupyter_server_config.py`

```bash
jupyter server --generate-config
```

### 2. Modify `jupyter_server_config.py`

#### Recommended settings :

```bash
ContentsManager.allow_hidden = True
# Hidden files and folders can be displayed in JupyterLab
```

### 3. Settings > Advanced Settings Editor > JSON Settings Editor

### 4. Set `"showHiddenFiles": true,` and SAVE

