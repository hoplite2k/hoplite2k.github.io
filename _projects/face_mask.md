---
layout: page
title: Face Mask Detector
description:
img: assets/img/facemask-1.jpeg
importance: 6
category: Academic
---

This repository contains a face-mask detector built using Tensorflow/keras and OpenCV

I have built a classifier whick classifies whether a image contains mask or not. The classifier is built using MobileNetV2 pre trained model. I have used OpenCV for real time video capture. For face detection I have used pre-trained caffemodel. For face detection you can refer my another repository, click <a href="">here</a>

I have already trained the classifier and saved the model in model directory. The model was trained by executing dnn_model.py

The mask_detector.py loads the trained model and uses OpenCV for real time video capture and feeds the frames to the model and predicts the output

To run the face detection module execute " python mask_detector.py " in your terminal or command prompt. Press esc to stop the program.

REQUIREMENTS:
    Tensorflow
    imutils
    OpenCV
    sklearn


<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/facemask-1.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/facemask-2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Images are taken from the internet.
</div>

Codebase: <a href="https://github.com/hoplite2k/face-mask-detector">https://github.com/hoplite2k/face-mask-detector</a>
