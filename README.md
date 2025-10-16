# Creating an empty scene
from: https://isaac-sim.github.io/IsaacLab/main/source/tutorials/index.html > https://isaac-sim.github.io/IsaacLab/main/source/tutorials/00_sim/create_empty.html

## Pre requisites

- Install Conda

- Create a Conda env inside an Ubuntu terminal that runs python 3.11 > compatible with IsaacSIM 5.0
```
conda create -n env_isaaclab python=3.11
conda activate env_isaaclab
```

- Install PyTorch
```
pip install torch==2.7.0 torchvision==0.22.0 --index-url https://download.pytorch.org/whl/cu128
```

- Install Isaac SIM 5.0
```
pip install "isaacsim[all,extscache]==5.0.0" --extra-index-url https://pypi.nvidia.com
```

- Test that Isaac SIM is properly installed
from: https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/binaries_installation.html#isaaclab-binaries-installation

On a Windows command prompt, run:
```
set ISAACSIM_PATH=[INSERT YOUR LOCAL PATH TO WHERE ISAAC SIM IS INSTALLED IN YOUR COMPUTER]
set ISAACSIM_PYTHON_EXE=%ISAACSIM_PATH%\python.bat
%ISAACSIM_PATH%\isaac-sim.bat
%ISAACSIM_PYTHON_EXE% -c "print('Isaac Sim configuration is now complete.')"
%ISAACSIM_PYTHON_EXE% %ISAACSIM_PATH%\standalone_examples\api\omni.isaac.core\add_cubes.py
```
-> **Documentation Mistakes** The original Nvidia documentation has "%ISAACSIM_PYTHON_EXE% %ISAACSIM_PATH%\standalone_examples\api\isaacsim.core.api\add_cubes.py" this is the wrong path. This command should be replaced by "%ISAACSIM_PYTHON_EXE% %ISAACSIM_PATH%\standalone_examples\api\omni.isaac.core\add_cubes.py"

It should launch Isaac SIM

## Install Isaac Lab
from: https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/index.html#local-installation > 
https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/pip_installation.html 






## Launch the Simulator

