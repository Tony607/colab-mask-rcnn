# [How to run Object Detection and Segmentation on a Video Fast for Free](https://www.dlology.com/blog/how-to-run-object-detection-and-segmentation-on-video-fast-for-free/)


# How to Run
## Colab
The easiest way is to open  [the colab notebook](https://drive.google.com/file/d/11yXcMidH2rmnvy5GxFAr0M_0mABr1M_-/view?usp=sharing).

The following instruction is optional and only useful if you want to run locally.

## Optionally, run Locally

Require [Python 3.5+](https://www.python.org/ftp/python/3.6.4/python-3.6.4.exe) and [Jupyter notebook](https://jupyter.readthedocs.io/en/latest/install.html) installed
### Clone or download this repo
```
git clone https://github.com/Tony607/colab-mask-rcnn
```
### Install required libraries
`pip3 install -r requirements.txt`

### Install pycocotools (Windows only)
Since this notebook already contains cells to install `pycocotools`  using Linux command. Alternatively if you are using Windows PC, you can install it manually.
*   NOTE: pycocotools requires [Visual C++ 2017 Build Tools](http://landinghub.visualstudio.com/visual-cpp-build-tools)
*   Clone this repo.
```
git clone https://github.com/philferriere/cocoapi.git
```
*   Use pip to install pycocotools.
```
pip install git+https://github.com/philferriere/cocoapi.git#subdirectory=PythonAPI
```

### Start the notebook
In the project start a command line run
```
jupyter notebook
```
In the opened browser window open
```
Colab_Mask_R_CNN_Demo.ipynb
```

