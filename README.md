# Creating an empty scene
from: https://isaac-sim.github.io/IsaacLab/main/source/tutorials/index.html > https://isaac-sim.github.io/IsaacLab/main/source/tutorials/00_sim/create_empty.html

## Pre requisites: Installing IsaacSIM and IsaacLAB

from: https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/index.html#local-installation > 
https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/pip_installation.html 

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

- Install Driver components inside the Ubuntu environment
  - Components
  - ```
    wget https://developer.download.nvidia.com/compute/cuda/repos/wsl-ubuntu/x86_64/cuda-wsl-ubuntu.pin
    sudo mv cuda-wsl-ubuntu.pin /etc/apt/preferences.d/cuda-repository-pin-600
    wget https://developer.download.nvidia.com/compute/cuda/12.5.0/local_installers/cuda-repo-wsl-ubuntu-12-5-local_12.5.0-1_amd64.deb
    sudo dpkg -i cuda-repo-wsl-ubuntu-12-5-local_12.5.0-1_amd64.deb
    sudo cp /var/cuda-repo-wsl-ubuntu-12-5-local/cuda-*-keyring.gpg /usr/share/keyring```
  - Remove error files
  - ```
    sudo rm /etc/apt/sources.list.d/devel:kubic:libcontainers:stable.list
    sudo apt-get update
    ```
  - 
    
  - Install the CUDA Toolkit:
  - ```
    sudo apt-get -y install cuda-toolkit-12-5
    ```
  - Install graphics drivers PPA
  - ```
    sudo add-apt-repository ppa:graphics-drivers/ppa
    sudo apt-get update
    sudo apt-get install nvidia-driver-550
    ```
  - Find and update the Vulkan driver
  - ```
    sudo find / -name "libnvidia-glvkspirv.so*" ```
  - IF the file installation worked it should output : "/usr/lib/x86_64-linux-gnu/libnvidia-glvkspirv.so.580.95.0"
  - Update the config file
  - ``` sudo nano /etc/vulkan/icd.d/nvidia_icd.json ```
  - replace with this
  - ```
    {
    "file_format_version": "1.0.0",
    "ICD": {
        "library_path": "/usr/lib/x86_64-linux-gnu/libnvidia-glvkspirv.so.580.95.05",
        "api_version": "1.3.250"
    }
  }
  ```
  ```
  - Exit save and close
  - shut down power shell: wsl --shutdown
  - Reboot computer












- Install Isaac SIM 5.0
```
pip install "isaacsim[all,extscache]==5.0.0" --extra-index-url https://pypi.nvidia.com
```

- Test that Isaac SIM is properly installed
```
isaacsim
isaacsim isaacsim.exp.full.kit
```

It should launch Isaac SIM








## Launch the Simulator

