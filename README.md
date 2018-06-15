# Keras implementation of Faster-RCNN

> This is a very userful implementation of faster-rcnn on Tensorflow and Keras. The model is very clear and just saved in a .h5 file format, out of box to use, and easy to train on other dataset with full support. If you have any question, feel free to ask me via wechat: jintianiloveu

## Requirements
Basically, this code supports both python2.7 and python3.5, the following package should be installed:
* tensorflow
* keras
* scipy
* cv2

On the command line, run the following, on requirements.txt, to install all the dependencies
```
for req in $(cat requirements.txt); do pip install $req; done
```

## Out of the box model to predict

I have trained a model to predict kitti. I will update a dropbox link here later. Let's see the result of predict:

<img src="http://opbocoyb4.bkt.clouddn.com/000010.png" align="center">

## Training a model on a Dataset

Training a new dataset is very simple and straightforward. Simply convert your detection label txt file (for example: kitti_simple_label.txt) into this format:

```
/path/training/000000.png,712.40,143.00,810.73,307.92,Pedestrian
/path/training/000001.png,599.41,156.40,629.75,189.25,Truck
```
Which is `/path/to/img.png,x1,y1,x2,y2,class_name`, with this simple file, we don't need class map file, our training program will learn this automatically.

## To predict detections

If you want to see how good your trained model is, simply run:
```
python test_frcnn_kitti.py
```
You can also use `-p` to specify a single image to predict, or send a path containing many images. Our program will automatically recognize that.

**That's all, help you enjoy!**
