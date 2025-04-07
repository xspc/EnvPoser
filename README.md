<div align="center">

<h1>EnvPoser: Environment-aware Realistic Human Motion Estimation from Sparse Observations with Uncertainty Modeling</h1>

<div>
    <a href='https://xspc.github.io/' target='_blank'>Songpengcheng Xia<sup></sup></a>&emsp;
    <a target='_blank'>Yu Zhang<sup></sup></a>&emsp;
    <a href='https://suzhuo.github.io/' target='_blank'>Zhuo Su<sup>*</sup></a>&emsp;
    <a target='_blank'>Xiaozheng Zheng<sup></sup></a>&emsp;
    <a target='_blank'>Zheng Lv<sup></sup></a>&emsp;
    <a target='_blank'>Guidong Wang<sup></sup></a>&emsp;
</div>
<div>
    <a target='_blank'>Yongjie Zhang<sup></sup></a>&emsp;
    <a href='https://sjtu-robotics.com/zh/' target='_blank'>Qi Wu<sup></sup></a>&emsp;
    <a href='https://scholar.google.com.hk/citations?user=HgZ0wNwAAAAJ&hl=zh-CN&oi=ao' target='_blank'>Lei Chu<sup></sup></a>&emsp;
    <a href='https://scholar.google.com.hk/citations?user=Vm7d2EkAAAAJ&hl=zh-CN&oi=ao' target='_blank'>Ling Pei<sup>†</sup></a>&emsp;
</div>
<div>
    Shanghai Jiao Tong University, ByteDance
</div>

<div>
    <sup>†</sup>Corresponding author &emsp; <sup>*</sup>Project Leader
</div>

<div>
    :star_struck: <strong>Accepted to CVPR 2025</strong>
</div>

<h4 align="center">
  <a href="https://www.youtube.com/watch?v=88_CyBNtEe8&t=168s" target='_blank'>[Demo]</a> •
  <a href="https://arxiv.org/abs/2412.10235" target='_blank'>[arXiv]</a>
</h4>

</div>

This is the pytorch implementation of our paper EnvPoser at CVPR 2025.


## Environment Setup

We tested our code on Windows with `Python 3.8.15`, `Pytorch 1.10.2` with `cuda11.1`, other dependencies are specified in `requirements.txt`.

```python
conda create -n dynaip python==3.8.15
conda activate envposer
pip install torch==1.10.2+cu111 torchvision==0.11.3+cu111 torchaudio==0.10.2 -f https://download.pytorch.org/whl/cu111/torch_stable.html
pip install -r requirements.txt
```

## Datasets and Models

### Datasets

We used publicly available EgoBody and GIMO datasets to train and evaluate our model. You can download the raw data from:

+ EgoBody: https://zenodo.org/records/3254403 


Clone this repo, download the above datasets, extract and place them in `./datasets/raw/`.

```python
datasets
├─extract
├─raw
│  ├─EgoBody
└─work
```

### SMPL Models

We used the smpl model, download it from [here](https://smpl.is.tue.mpg.de) and place in  `./smpl_models/`.

```python
smpl_models
    smpl_female.pkl
    smpl_male.pkl
    smpl_neutral.pkl
```

## Data Processing

1. 

## Training and Evaluation

For training and evaluation, simply run:

```python
python train.py
python evaluation.py
```

The pretrained weights are stored in `./weights` folder.

## Visualization

We use `aitviewer` for visualization, run:

```python
python vis.py
```

for visualizing the predicted results.

## Acknowledgement

Some of our codes are adapted from [PIP](https://github.com/Xinyu-Yi/PIP) and [EgoHMR](https://github.com/sanweiliti/EgoHMR).

## Citation

If you find this project helpful, please consider citing us:

```
@article{xia2024envposer,
  title={EnvPoser: Environment-aware Realistic Human Motion Estimation from Sparse Observations with Uncertainty Modeling},
  author={Xia, Songpengcheng and Zhang, Yu and Su, Zhuo and Zheng, Xiaozheng and Lv, Zheng and Wang, Guidong and Zhang, Yongjie and Wu, Qi and Chu, Lei and Pei, Ling},
  journal={ IEEE / CVF Computer Vision and Pattern Recognition Conference (CVPR)},
  year={2025},
  publisher={IEEE},
  booktitle={cvpr}
}
```
