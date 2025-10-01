# YOLO11 Inference on MacBook Air M1 vs. NVIDIA Jetson Orin Nano

## Intro
YOLO (You Only Look Once) is a real-time object detection algorithm based on convolutional neural networks.
I am using in my project to detect maritime objects such as boats, buoys, lighthouses and windfarms.
The NVIDIA Jetson is an embedded computing board specialized for accelerating neural networks.
It used alot in robot applications for real-time inference. With 300€ it is quite cheap for its power and is well documentated.

![YOLO detecting a Sailboat](/docs/assets/images/yolo_boat.gif)

## Goal

Quick test what inference times are possible on the different hardwares using different model sizes and types.

## Setup

- NVIDIA Jetson Orin Nano
- MacBook Air M1
- Model: YoloV11
- Size: Nano, Small
- Model formats: Open Neural Network Exchange _.onnx_, TensorRt  _.engine_, Pytorch _.pt_

For the Jetson Nano there are many tips and tricks to [improve the performance](https://docs.ultralytics.com/guides/nvidia-jetson/). The command __jetson_clocks__ had the most significant improvement on the inference time improving it by factor 2.\

## Results

First things first: This is not a fair fight! Running a Deep Neural Network (short __DNN__) on a standard laptop versus on a dedicated platform for accelerating neural networks.
The following measurements show the average inference times.

![YOLO11N Inference Time](/docs/assets/images/yolo11n_time.png)
![YOLO11S Inference Time](/docs/assets/images/yolo11s_time.png)

__Key take-aways:__

- The NVIDIA Jetson Orin Nano achieves faster inference times.
- PyTorch optimizes inference for the M1 GPU making it 2x faster than running on the CPU.
- The inference times can be optimized on the NVIDIA Jetson by using half the floating point precision (FP16).
- On the M1 you cannot use half precision to optimize the runtime.
- _ONNX_ format does not run on M1 GPU but only on the CPU. 

## Training on Jetson Nano

It is possible to train the Yolo11 model on the Jetson Nano. However, the RAM is not sufficient for large models or batch sizes. Also for a large number of epochs >20 the training time will be several hours or days.
I would suggest using the Jetson Nano for a quick check if the training data and model work. For training on large data sets and for larger epochs a GPU with more memory and speed is necessary.
The following configurations worked reasonably well:

- Yolo11 Nano, Batch size 8
- Yolo11 Small, Batch size 1
- Epochs <20

## Summary

The NVIDIA Jetson Orin Nano has the GPU power to run real-time object detection with YOLO11. With a price of only 300€ this is the go to hardware for our real-time detection of sailboats. However, for developing and testing the application the MacBook Air is fast enough and offers more convenience.

## Outlook

In the next steps the model will be fine-tuned to detect other maritime objects such as buoys, light houses and wind farms.
I will also take a look at how larger models perform on detecting these objects. For training larger models the NVIDIA Jetson Orin Nano
does not have enough RAM. A training on cloud based GPU will be used instead.
