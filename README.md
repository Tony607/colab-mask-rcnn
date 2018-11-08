# [How to run Object Detection and Segmentation on a Video Fast for Free](https://www.dlology.com/blog/how-to-run-object-detection-and-segmentation-on-video-fast-for-free/)

![alt text](https://gitcdn.xyz/cdn/Tony607/blog_statics/23cd63466316e14d91998bf6aeb47f8d660f4378/images/colab/out-clip.gif  "Video Demo")
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



## Error in google colab notebook

  You might see error like`AttributeError: module 'keras.engine.topology' has no attribute 'load_weights_from_hdf5_group_by_name'`, because in colab notebook, you are using an old version() Mask_RCNN`2.0` version)  That's why you changed git branch`!git checkout 555126ee899a144ceff09e90b5b2cf46c321200c`

```python
## This is the line that causes the error.
model.load_weights(COCO_MODEL_PATH, by_name=True)
```



So, This error is solved this way.

1. Change to [mode.py](model.py) on `/content/Mask_RCNN/model.py`
2. Save (Ctrl + S) in google colab notebook.
3. That's it, then you can use `model.load_weights` function.