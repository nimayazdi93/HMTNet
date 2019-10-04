# Hierarchical Multi-Task Network For Race, Gender and Facial Attractiveness Recognition
## Introduction
This repository holds the PyTorch implementation of our paper [Hierarchical Multi-Task Network For Race, Gender and Facial Attractiveness Recognition](https://ieeexplore.ieee.org/abstract/document/8803614).

![HMTNet](./hmt_architecture.png)

## How to use
* Install 3rd party libraries   
    ````sudo pip3 install -r requirements.txt````
* Modify [cfg.py](./config/cfg.py) to fit your path


## Hyper-param Selection
| Loss | MAE | RMSE | PC | Acc_R | Acc_G| Epoch | WD |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| MSE | 0.2556 | 0.3372 | 0.8693 | 99.68% | 98.53% | 170 | 5e-2|
| L1 | 0.2500 | 0.3299 | 0.8753 | 99.26% | 98.16% | 150 | 5e-2|
| Smooth L1 | 0.2531 | 0.3313 | 0.8738 | 99.54% | 98.58% | 170 | 5e-2|
| Smooth Huber | 0.2501 | 0.3263 | 0.8783 | 99.26% | 98.16% | 170 | 5e-2|
| **FiveCrops (New)** | 0.2439 | 0.3226 | 0.8801 | 99.45% | 98.58% | 149 | 5e-2|


## Performance Comparison
| Methods | MAE | RMSE | PC |
| :---: | :---: | :---: | :---: |
| ResNeXt-50 | 0.2518 | 0.3325 | 0.8777 |
| ResNet-18 | 0.2818 | 0.3703 | 0.8513 |
| AlexNet | 0.2938 | 0.3819 | 0.8298 |
| CRNet | 0.2816 | 0.3669 | 0.8450 |
| **HMTNet (Ours)** | **0.2500** | **0.3299** | **0.8753** |
| **HMTNet (Ours)** | **0.2501** | **0.3263** | **0.8783** |
| **HMTNet (Ours)** | **0.2439** | **0.3226** | **0.8801** |


**New:** By leveraging ``FiveCrops`` inference, we are able to achieve better
 performance at ``129th Epoch``! 


## Samples
![Prediction](./fbp_pred.png)

![TikTok Video](./TikTok.gif)

## Deep Feature Visualization
![Feature Visualization](./feature_vis.png)


## Citation
If you find this repository helps your research, please cite our paper:
```
@inproceedings{xu2019hierarchical,
  title={Hierarchical Multi-Task Network For Race, Gender and Facial Attractiveness Recognition},
  author={Xu, Lu and Fan, Heng and Xiang, Jinhai},
  booktitle={2019 IEEE International Conference on Image Processing (ICIP)},
  pages={3861--3865},
  year={2019},
  organization={IEEE}
}
```
