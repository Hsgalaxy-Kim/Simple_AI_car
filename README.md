# Simple_AI_car

## lecture : Intelligent control
[2022] This repo is Simple_AI_car project. **Using raspberry pi 4,** the goal is to complete the car along a given track. 
* track
<img width="50%" src="https://user-images.githubusercontent.com/101552457/204456144-072e2a0d-366f-4e54-bed2-4f08a5c92178.jpeg"/>

## Required Library
* python 3.6.13
* tensorflow 2.3.0
* tensorflow-gpu 2.3.0

## Dataset
* [Download](https://drive.google.com/file/d/1-3JE-Lxqr8hpYcCbfAfr5NvojXgQPt_d/view?usp=sharing)

## Training data sample
* Going straight
<img width="20%" src="https://user-images.githubusercontent.com/101552457/204458797-27e5252c-49cb-497f-8a0f-0206b32f622f.png"/>

* Truning right
<img width="20%" src="https://user-images.githubusercontent.com/101552457/204458832-ee1efe13-a0a3-468e-a4a7-2c7ec388a93d.png"/>

* Truning left
<img width="20%" src="https://user-images.githubusercontent.com/101552457/204458869-7d9737d5-dd4d-4da7-8096-2a16e603d256.png"/>

## Issue & Solution
Original model is Nvidia model. I modified this model to reduce size(parameter). I expected this modification to improve the response speed of the model. **However, Reduction of model size resulted in a decrease in generalization capability.** So there was a problem that it didn't work where the lighting was weak. **For normal operation, I found that using multi-threads rather than speed improvement through the size of the model is the correct solution. In addition, creating low-light image data augmatation will greatly help improve performance.**
