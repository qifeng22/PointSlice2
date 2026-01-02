# PointSlice
This repository contains the official implementation of the **PointSlice** model, offering an innovative **3D object detection method**. You can use the following approaches to utilize it.

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

For detailed package versions, please see our [requirements.txt](requirements.txt).
### **Install pcdet**
Please install the `pcdet` library and its dependencies by running:

```bash
python setup.py develop
```


## **Usage**
To begin, please follow the [HEDNet Getting Started Guide](https://github.com/zhanggang001/HEDNet/blob/main/docs/GETTING_STARTED.md) to download and prepare the dataset. **Note that this process requires significant disk space and time.**

Once the data is ready, you can run the code using the following command:
### Waymo
```
bash scripts/dist_train.sh cfgs/pointslice/pointslice_1f_1x_waymo.yaml 8 --batch_size 16 --epoch 24 --workers=2
```
![image](https://github.com/qifeng22/PointSlice2/raw/main/waymo.png)

You can evaluate the model's performance using the following command:

```bash
python test.py --cfg_file cfgs/pointslice/pointslice_1f_1x_waymo.yaml --ckpt {yourckpt.pth path} --batch_size 1
```
### nuScenes
For nuScenes code, you can refer to [this GitHub repository](https://github.com/qifeng22/PointSlice-nuscenes/tree/main).

## **Acknowledgement**

Our code is based on [OpenPCDet](https://github.com/open-mmlab/OpenPCDet) and [HEDNet](https://github.com/zhanggang001/HEDNet). We thank the authors for their open-source contribution.





