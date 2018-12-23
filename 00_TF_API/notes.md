# Using TensorFlow's Object Detection API

This chapter introduces you to the [TensorFlow's Object Detection API](https://github.com/tensorflow/models/blob/master/research/object_detection), which is a repository with trained object detection models.

This may be the easiest way to get and object detection system up and running. It may even work pretty well on several circumstances, specially if your dataset is similar to those in which the provided models have been trained on (see the [official model zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/detection_model_zoo.md)).

In this chapter has two goals:
* To show you how to use an off-the-shelf model and to evaluate it so that you can see if you require to finetune the model for your particular dataset.
* To show you how to finetune a provided model for your particular needs.

To achive both of the previous goals we need a dataset to work on. We will be working with data from the  [Multiple Object Tranking Benchmark](https://motchallenge.net/) (2D MOT 2015), although we may not use all of it.

Before we start, make sure you add the project directory to the PYTHONPATH variable:

```
# From root project directory
export PYTHONPATH=$PYTHONPATH:`pwd`
```
Otherwise, the API would not work.

## Understanding our data

It is very important to explore our dataset first. Download the data from [this link](https://motchallenge.net/data/2DMOT2015.zip) (if you don't trust the link, or they move the data elsewhere, find the 2D MOT 2015 data and download it) and put the `train` and `test` folders inside dataset. Then go to the [exploration](dataset/exploration.ipynb) notebook before moving to the other sections.

## Using an off-the-shelf detector

All instructions for runing an off-the-shelf detector are in the [off-the-shelf notebook](off_the_shelf.ipynb), please read it thoroughly.

## Finetuning a detector

This task is a bit more complicated. To start, we need to format the training data in the way that is expected by the API.