# GlueStick
Joint deep matcher for points and lines 🖼️💥🖼️

![Visualization of point and line matches](resources/demo_seq1.gif)

This repository contains the official implementation of 
[GlueStick: Robust Image Matching by Sticking Points and Lines Together](#).

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
```

## Running GlueStick 🏃
Download the weights of the model:
```
pip install gdown
gdown -O resources/weights/checkpoint_GlueStick_MD.tar https://drive.google.com/uc?id=1Gw26jVaU9fwOemQ3jBVINdJFdMXpV8Qv&export=download
```

You can execute the inference with it with:
```
python -m gluestick.run -img1 resources/img1.jpg -img2 resources/img2.jpg
```

## Training 🏋️
We want to provide you with high-quality and flexible code for training. Stay tuned, we will release it soon!

## Citation 📝
If you use this code in your project, please consider citing the following paper:
```bibtex
@article{pautrat_suarez_2023_gluestick,
    title={{GlueStick}: Robust Image Matching by Sticking Points and Lines Together},
    author={Pautrat, R{\'e}mi* and Su{\'a}rez, Iago* and Yu, Yifan and Pollefeys, Marc and Larsson, Viktor},
    journal={ArXiv},
    year={2023}
}
```
