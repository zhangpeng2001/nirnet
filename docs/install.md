<p align="center">
  <h1 align="center">Installation & Dataset
  </h1>
</p>

## Installation 🔥

### Requirements :hourglass:

- Linux
- Python 3.8.16
- PyTorch 1.11.0
- CUDA 11.3
- GCC 7.5.0

We have verified that the above settings run the program properly.

### Install NIRNet :mega:

a. Create a conda virtual environment and activate it.

```shell
conda create -n nirnet python=3.8.16
conda activate nirnet
```

b. Install PyTorch and torchvision following the [official instructions](https://pytorch.org/), e.g.,

```shell
conda install pytorch==1.11.0 torchvision==0.12.0 torchaudio==0.11.0 cudatoolkit=11.3 -c pytorch
```

Note: Make sure that your compilation CUDA version and runtime CUDA version match.
You can check the supported CUDA version for precompiled packages on the [PyTorch website](https://pytorch.org/).

c. Install MMCV following the [official instructions](https://github.com/open-mmlab/mmcv), e.g.,

```shell
install mmcv
```

d. Clone the DADet repository.

```shell
git clone https://github.com/zhangpeng2001/nirnet
cd nirnet
```

e. Install build requirements and then install DADet.

```shell
pip install -r requirements/build.txt
pip install -v -e .
```

## Dataset Preparation 🔥
Hazy-DIOR shares the training set and labels with standard [DIOR](https://gcheng-nwpu.github.io/#Datasets) dataset. We will release the whole dataset in the near future.

### Dataset Examples :notebook:

![dataset](../source/dataset.jpg)

### Dataset Documents :open_file_folder:

```shell
hazy_dior
├── Annotations
│   ├──00001.xml
│   ├──00002.xml
│   ...
│   └──xxxxx.xml
|
├── ImageSets
│   ├── Main
│       ├──train.txt
│       ├──val.txt
│       ├──trainval.txt
│       └──test.txt
|
├── JPEGImages
    ├──00001.jpg
    ├──00002.jpg
    ...
    └──xxxxx.jpg

```

### Citation :bulb:
If you use DIOR dataset in your research, please cite the following information.
```tex
@article{RN37,
   author = {Li, Ke and Wan, Gang and Cheng, Gong and Meng, Liqiu and Han, Junwei},
   title = {Object detection in optical remote sensing images: A survey and a new benchmark},
   journal = {ISPRS Journal of Photogrammetry and Remote Sensing},
   volume = {159},
   pages = {296-307},
   ISSN = {0924-2716},
   DOI = {10.1016/j.isprsjprs.2019.11.023},
   year = {2020},
   type = {Journal Article}
}

@misc{cheng2021,
  title={Anchor-free Oriented Proposal Generator for Object Detection}, 
  author={Gong Cheng and Jiabao Wang and Ke Li and Xingxing Xie and Chunbo Lang and Yanqing Yao and Junwei Han},
  year={2021},
  eprint={2110.01931},
  archivePrefix={arXiv},
  primaryClass={cs.CV}
}
```


