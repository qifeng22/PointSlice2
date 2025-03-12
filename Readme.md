The repositories offer an interesting 3D object detection method. You can use the following methods to utilize it.
## **Installation Guide**

This document provides a step-by-step guide to installing the required dependencies and setting up the environment for running the project.

### **Requirements**
The code has been tested in the following environments:

- **Operating System**: Linux (Ubuntu 20.04)
- **Python**: 3.6+
- **PyTorch**: 1.1 or higher 
- **CUDA**: 9.0 or higher (PyTorch 1.3+ requires CUDA 9.2+)
- **Sparse Convolution Library**: `spconv`
  - `spconv v1.0` (commit **8da6f96**) for PyTorch 1.1
  - `spconv v1.2` for PyTorch 1.3+
  - `spconv v2.x` (latest version, install via `pip`)


## **Usage**
Our code based on the Openpcdet and HEDNet, you can run this code by the following commmad
### Waymo
```
bash scripts/dist_train.sh cfgs/pointslice/pointslice_1f_1x_waymo.yaml 8 --batch_size 16 --epoch 24 --workers=2
```
![image](https://github.com/qifeng22/PointSlice2/raw/main/waymo.png)
### nuScenes


