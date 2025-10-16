# Creating an empty scene
from: https://isaac-sim.github.io/IsaacLab/main/source/tutorials/index.html > https://isaac-sim.github.io/IsaacLab/main/source/tutorials/00_sim/create_empty.html

## Install Isaac Lab
from: https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/index.html#local-installation > https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/binaries_installation.html#isaaclab-binaries-installation 

- Test that Isaac SIM is properly installed

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

- Installing Isaac Lab



## Launch the Simulator

