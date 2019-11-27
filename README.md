# CarND Object Detection Lab

![](assets/clip.gif)

In lab this you will:

* Learn about *MobileNets* and separable depthwise convolutions.
* The SSD (Single Shot Detection) architecture used for object detection
* Use pretrained TensorFlow object detection inference models to detect objects
* Use different architectures and weigh the tradeoffs.
* Apply an object detection pipeline to a video.

Open the notebook and work through it!

### Requirements

Install environment with [Anaconda](https://www.continuum.io/downloads):

```sh
conda env create -f env_cn.yml
```

Change TensorFlow pip installation from `tensorflow-gpu` to `tensorflow` if you don't have a GPU available.

The environment should be listed via `conda info --envs`:

```sh
# conda environments:
#
carnd-advdl-odlab        /usr/local/anaconda3/envs/carnd-advdl-odlab
root                  *  /usr/local/anaconda3
```

Activate
```sh
conda activate carnd-advdl-odlab
```

Deactivate
```sh
conda deactivate
```

Further documentation on [working with Anaconda environments](https://conda.io/docs/using/envs.html#managing-environments). 

Particularly useful sections:

https://conda.io/docs/using/envs.html#change-environments-activate-deactivate
https://conda.io/docs/using/envs.html#remove-an-environment

### Resources

* TensorFlow object detection [model zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/detection_model_zoo.md)
* [Driving video](https://s3-us-west-1.amazonaws.com/udacity-selfdrivingcar/advanced_deep_learning/driving.mp4)

### Use Tensorflow maps

Download
```sh
wget --tries=3 "download.tensorflow.org/models/object_detection/ssd_mobilenet_v1_coco_11_06_2017.tar.gz"
wget --tries=3 "download.tensorflow.org/models/object_detection/rfcn_resnet101_coco_11_06_2017.tar.gz"
wget --tries=3 "download.tensorflow.org/models/object_detection/faster_rcnn_inception_resnet_v2_atrous_coco_11_06_2017.tar.gz"
```

Extract
```sh
tar xf ssd_mobilenet_v1_coco_11_06_2017.tar.gz
tar xf rfcn_resnet101_coco_11_06_2017.tar.gz
tar xf faster_rcnn_inception_resnet_v2_atrous_coco_11_06_2017.tar.gz
```

### Tips
- Some windows users have reported the driving video as playable only in Jupyter Notebook operating in Chrome browser, and not in media player or Jupyter Notebook operating in other browsers.  In contrast the post-segmentation video appears to be operating across players and browsers.
