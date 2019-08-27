# [How to train an object detection model easy for free](https://www.dlology.com/blog/how-to-train-an-object-detection-model-easy-for-free/) | DLology Blog



## How to Run

Easy way: run [this Colab Notebook](https://colab.research.google.com/github/MorganJ101/void_detection/blob/master/void_detection_training_colab.ipynb).

Alternatively, if you want to use your images instead of ones comes with this repo.

Require [Python 3.5+](https://www.python.org/ftp/python/3.6.4/python-3.6.4.exe) installed.
### Fork and clone this repository to your local machine.
```
https://github.com/MorganJ101/void_detection
```
### Install required libraries
`pip3 install -r requirements.txt`


### Step 1: Annotate some images
- Save some photos with your custom object(s), ideally with `jpg` extension to `./data/raw` directory.
- Resize those photo to uniformed size. e.g. `(800, 600)` with
```
python resize_images.py --raw-dir ./data/raw --save-dir ./data/images --ext jpg --target-size "(800, 600)"
```
Resized images locate in `./data/images/`
- Train/test split those files into two directories, `./data/images/train` and `./data/images/test`

- Annotate resized images with [labelImg](https://tzutalin.github.io/labelImg/), generate `xml` files inside `./data/images/train` and `./data/images/test` folders. 

*Tips: use shortcuts (`w`: draw box, `d`: next file, `a`: previous file, etc.) to accelerate the annotation.*

- Commit and push your annotated images and xml files (`./data/images/train` and `./data/images/test`) to your forked repository.


### Step 2: Open [Colab notebook](https://colab.research.google.com/github/MorganJ101/void_detection/blob/master/void_detection_training_colab.ipynb)
- Replace the repository's url to yours and run it.


## Commendations
This repo was helped by following the User Tony607 on Github.
See: https://github.com/Tony607/object_detection_demo
