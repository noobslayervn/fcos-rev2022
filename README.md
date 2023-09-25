# Specification

- Wsl windows
- Ubuntu 18.04.6 LTS
- conda 22.11.1
- Python 3.8.15

## nvidia-smi
- NVIDIA-SMI 525.60.12
- Driver Version: 527.41
- CUDA Version: 12.0

## torch
- 1.13.1
- True
- 1
- 0
- <torch.cuda.device object at 0x7f8946396730>
- NVIDIA GeForce RTX 3060 Laptop GPU
- 11.6

## conda list python
ipython                   8.7.0            py38h06a4308_0  
ipython_genutils          0.2.0                      py_1    conda-forge
opencv-python             4.5.3.56                 pypi_0    pypi
python                    3.8.15               h7a1cb2a_2  
python-dateutil           2.8.2              pyhd8ed1ab_0    conda-forge
python-fastjsonschema     2.16.2             pyhd8ed1ab_0    conda-forge
python_abi                3.8                      2_cp38    conda-forge

# Changes

## 1. Change vision.h path

- miniconda3\envs\fcos\FCOS\fcos_core\csrc\cpu\ROIAlign_cpu.cpp
- miniconda3\envs\fcos\FCOS\fcos_core\csrc\cpu\nms_cpu.cpp

## 2. Change PY3 version for recent pytorch

- miniconda3\envs\fcos\FCOS\fcos_core\utils\imports.py

## 3. Model zoo import name

- miniconda3\envs\fcos\FCOS\fcos_core\utils\model_zoo.py

## 4. Cuda file update

AT_CHECK into TORCH_CHECK
- miniconda3\envs\fcos\FCOS\fcos_core\csrc\cuda\deform_conv_cuda.cu
- miniconda3\envs\fcos\FCOS\fcos_core\csrc\cuda\deform_pool_cuda.cu

THC deprecated into Aten
- miniconda3\envs\fcos\FCOS\fcos_core\csrc\cuda\ROIPool_cuda.cu
- miniconda3\envs\fcos\FCOS\fcos_core\csrc\cuda\ROIAlign_cuda.cu
- miniconda3\envs\fcos\FCOS\fcos_core\csrc\cuda\SigmoidFocalLoss_cuda.cu
- miniconda3\envs\fcos\FCOS\fcos_core\csrc\cuda\nms.cu
- miniconda3\envs\fcos\FCOS\fcos_core\csrc\cuda\ml_nms.cu

## 5. Modeling rpn opencv

- miniconda3\envs\fcos\FCOS\fcos_core\modeling\rpn\inference.py
- miniconda3\envs\fcos\FCOS\fcos_core\modeling\rpn\fcos\inference.py

## 6. OpenCV putText changes

- miniconda3\envs\fcos\FCOS\demo\predictor.py
- miniconda3\envs\fcos\FCOS\fcos\fcos.py

## 7. Disable pytorch cuda 

I forgot...

## 8. Import external file

- Get from https://github.com/chei90/RemoteRendering/tree/master/inc
- miniconda3\envs\fcos\lib\python3.8\site-packages\torch\include\ATen\cusolver_common.h
- miniconda3\envs\fcos\lib\python3.8\site-packages\torch\include\ATen\cusolverDn.h
- miniconda3\envs\fcos\lib\python3.8\site-packages\torch\include\ATen\cusolverRf.h
- miniconda3\envs\fcos\lib\python3.8\site-packages\torch\include\ATen\cusolverSp.h