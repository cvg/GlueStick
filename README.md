# GlueStick
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cvg/GlueStick/blob/main/gluestick_matching_demo.ipynb) [![arXiv](https://img.shields.io/badge/arXiv-2304.02008-b31b1b.svg?style=flat)](https://arxiv.org/abs/2304.02008) [![Project Page](https://badgen.net/badge/color/project/green?icon=awesome&label)](https://iago-suarez.com/gluestick)

Joint deep matcher for points and lines 🖼️💥🖼️

**Update: we are pleased to announce that the training code has been released within our new training framework, [GlueFactory](https://github.com/cvg/glue-factory).**

![Visualization of point and line matches](resources/demo_seq1.gif)

This repository contains the official implementation of 
[GlueStick: Robust Image Matching by Sticking Points and Lines Together](https://arxiv.org/abs/2304.02008), accepted at ICCV 2023.

## Install 🛠️

To install the software in Ubuntu 22.04 follow these instructions:
```bash
sudo apt-get install build-essential cmake libopencv-dev libopencv-contrib-dev
git clone --recursive https://github.com/cvg/GlueStick.git
cd GlueStick
# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
pip install -e .
```

## Running GlueStick 🏃
Download the weights of the model:
```
wget https://github.com/cvg/GlueStick/releases/download/v0.1_arxiv/checkpoint_GlueStick_MD.tar -P resources/weights
```

You can execute the inference with it with:
```
python -m gluestick.run -img1 resources/img1.jpg -img2 resources/img2.jpg
```

## Training 🏋️
The training code is available in a separate repository, [GlueFactory](https://github.com/cvg/glue-factory). Within GlueFactory, you can not only train GlueStick, but also other deep matchers such as [LightGlue](https://github.com/cvg/LightGlue), use multiple feature extractors, line extractors, robust estimators, as well as run evaluations on multiple benchmarks.

## Licence 📜
Our code is licenced under [MIT licence](https://github.com/cvg/GlueStick/blob/main/LICENSE).
However, bear in mind that it uses a SuperPoint backbone that has a 
[non-commercial licence](https://github.com/magicleap/SuperPointPretrainedNetwork/blob/master/LICENSE). 
Therefore, the overall system is non-commercial 😞. We are working on an analogous version based on 
[DISK](https://github.com/cvlab-epfl/disk) to avoid this problem.

## Citation 📝
If you use this code in your project, please consider citing the following paper:
```bibtex
@InProceedings{pautrat_suarez_2023_gluestick,
    title={{GlueStick}: Robust Image Matching by Sticking Points and Lines Together},
    author={Pautrat, R{\'e}mi* and Su{\'a}rez, Iago* and Yu, Yifan and Pollefeys, Marc and Larsson, Viktor},
    booktitle={International Conference on Computer Vision (ICCV)},
    year={2023}
}
```
