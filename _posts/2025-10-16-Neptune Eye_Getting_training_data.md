# Neptune's Eye: Hoisting the sails to get data

## Introduction

Introducing __Neptune's Eye__. This is the beginning of a new open source project. The goal is to develop a real-time object detection system that detects hazards such as other boats, buoys or fishing traps for safer sailing.\

__Step 1: Collecting Data__
When building an object detection model, running the actual training is the easy part. The hard part is acquiring a
dataset that fits your application. The quality of the data influences the quality of the detection significantly.
Finding a dataset for cats, dogs or cars is easy. But finding data for detecting buoys, boats, fishing traps and other
hazards that we run into during sailing is not trivial.

![Neptune Eye](/docs/assets/images/neptune_eye_ai.png)\
*Neptune's Eye AI generated image*

## Goal

Acquire good data to tain the model. In the first iteration the model should detect ships, buoys and maybe fishing traps.
These classes present the main dangers at see. In the future, different ship classes like sailboats, small boats or freighters can trained, as well as new classes like light houses and wind farms.

## Getting data

### Public data

_Roboflow_ is a widely used plattform for vision data sets. I could not find a dataset that exactly fits my needs.
This means I had to create my own dataset from different sources. I could find a good dataset for buoys with about 300 images. This is not a lot but should be enough for initial testing. Buoys vary greatly in shape so a larger dataset will
probably be necessary in the future.\
The Yolo11 object detection was initially trained on the _COCO_ dataset. Since the detection of boats already worked very well with this pretrained model, I decided to take boat images from the _COCO_ dataset. I manually went through the first
couple of hundred of boat images to find those that match the application best. For Neptune Eye, boats will usually appear far away and be quite small. There are hopefully no close ups of boats, since this means a crash.

![COCO Boat 1](/docs/assets/images/coco_boat_1.jpg)![COCO Boat 2](/docs/assets/images/coco_boat_2.jpg)\
*COCO images of boats vary. Close-up on land or far away on the horizon*

### Hoisting the sails

The best data however, is the one taken directly from the boat. While sailing in October I took as many pictures of buoys and sailboats that I could get in a 4 days of sailing. This resulted in about 60 images of mostly buoys.
I used Label Studio to easily label these images manually. This worked fine for this small dataset. In the future I plan on using semi-automated labelling.

![Buoy](/docs/assets/images/buoy_label_studio.png)![Sailboat](/docs/assets/images/sailboat_label_studio.png)\
*Buoy and sailboat image taken from sailboat*


## Result

As a result I created a data set with about 900 boat and 300 buoy images. I only have a handful of fishing trap fotos and could not find anything on the internet.

## Summary

Collecting data is a more challenging and time consuming task. Since it is winter and the boat is on land
I will not be able to collect more _real_ data until next spring. For getting more images of the tricky fishing traps
I will need to be more creative. Scraping the internet or AI generated images for example.
