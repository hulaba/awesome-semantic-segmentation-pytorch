# Awesome Semantic Segmentation on PyTorch

<p align="center"><img width="70%" src="datasets/ADE_demo_img.png" /></p>

--------------------------------------------------------------------------------
This project aims at providing a concise, easy-to-use, modular reference implementation for semantic segmentation models using PyTorch.

## Update
- Move ```./weights``` to ```～/.torch/models```
- Add ResnetV1b
- Add lr scheculer

## Requisites
- [PyTorch 1.0](https://pytorch.org/get-started/locally/)
- Python 3.x

## Usage
#### Train
```
python train.py --model fcn32s --backbone vgg16 --dataset pascal_voc
```
#### Evaluation
```
python eval.py --model fcn32s --backbone vgg16 --dataset pascal_voc
```
#### Run Demo
```
python demo.py --model fcn32s_vgg16_voc --input-pic ./datasets/test.jpg
```
## Model Zoo & Datasets
#### Supported Model
- [FCN](https://arxiv.org/abs/1411.4038)
- [PSPNet](https://arxiv.org/pdf/1612.01105.pdf)

#### Supported Dataset
You can run script to download dataset, such as:
```
cd ./datasets
python ade20k.py --download-dir ./datasets/ade
```
- VOC2012, [download](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar)
- VOCAug, [download](http://www.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/semantic_contours/benchmark.tgz)
- ADK20K, [download](http://groups.csail.mit.edu/vision/datasets/ADE20K/)
- Cityscapes, [download](https://www.cityscapes-dataset.com/downloads/)
- COCO

## Result
#### PASCAL VOC 2012
|Methods|Backbone|TrainSet|EvalSet|Mean IoU|pixAcc|
|:-:|:-:|:-:|:-:|:-:|:-:|
|FCN32s|VGG16|train|val|47.50%|85.39%|
|FCN16s|VGG16|train|val|49.16%|85.98%|
|FCN16s|VGG16|train|val|48.87%|85.02%|

## To Do
- [ ] Add more semantic segmentation models (in process)
- [ ] Train process
- [ ] Find difference between ```cuda``` and ```only cpu```
- [ ] Why is the performance so terrible?
