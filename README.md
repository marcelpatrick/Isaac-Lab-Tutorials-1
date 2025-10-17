# Creating an empty scene
from: https://isaac-sim.github.io/IsaacLab/main/source/tutorials/index.html > https://isaac-sim.github.io/IsaacLab/main/source/tutorials/00_sim/create_empty.html

## Pre requisites

- Install Conda
- Install Ubuntu 
- open an Ubuntu CLI terminal
- Create a Conda env inside an Ubuntu terminal that runs python 3.11 > compatible with IsaacSIM 5.0
```
conda create -n env_isaaclab python=3.11
conda activate env_isaaclab
```

- Install PyTorch
```
pip install torch==2.7.0 torchvision==0.22.0 --index-url https://download.pytorch.org/whl/cu128
```

- Install Vulkan tools
```
sudo apt install vulkan-tools
```

- Make sure you have the latest NVIDIA driver installed
. check it here: https://www.nvidia.com/en-us/drivers/

- Install Isaac SIM 5.0
```
pip install "isaacsim[all,extscache]==5.0.0" --extra-index-url https://pypi.nvidia.com
```

- Test that Isaac SIM is properly installed




It should launch Isaac SIM

## Install Isaac Lab
from: https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/index.html#local-installation > 
https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/pip_installation.html 






## Launch the Simulator

