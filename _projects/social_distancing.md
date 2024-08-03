---
layout: page
title: Social Distancing Detector
description:
img: assets/img/social-1.jpeg
importance: 1
category: Academic
---

During this ongoing COVID-19 pandemic, social distancing is considered as a vital measure to contain the spreading of the disease. To limit the spread of an infectious disease, for instance, Covid-19, one of the most recommended measures is to practice social distancing. This is not a novel concept; for many generations, most communities have recognised the importance of staying away from those who are sick.
To relieve pressure on the healthcare system, the goal is to limit transmission by postponing the epidemic peak, reducing the size of the epidemic peak, and spreading cases over a longer period of time. It is a method of limiting one's contact with other people. It has been indicated that keeping a distance of around 2 metres between yourself and another person reduces the transmission of most flu virus strains, including COVID 19.

Even after many proposed interventions and measures taken by the government, there are a lot of instances where social distancing norms are violated. There are approaches using bluetooth and mobile phones to check for social distancing violation, but it requires an app to be installed. 
The proposed system implements image processing and uses various methods of object detection. The input for the model would be a video stream and the output will be a video containing all the violations that are detected and bounding boxes marked across them in case of violations.

a) Object detection : The model uses OpenCV and YOLO for image processing and object detection. The libraries used are open source. The MobileNet Single Shot Multibox Detector (SSD) object detection model and the OpenCV library for image processing are used in this study to detect social distance between people in areas of interest. YOLO is a state-of-the-art, real-time object detection system. Single Shot detector(SSD) like YOLO takes just one shot to detect multiple objects present in a picture using a multibox. It is a high-accuracy object detection algorithm and significantly faster in speed.
b) Computing pairwise distance : Once the objects are detected and classified, centroids are calculated. To calculate the distance between two people, Euclidean Distance is calculated. Euclidean Distance is the minimum distance between any two points on a given plane. It's the distance of the line segment drawn between those two points.
c) Visualization : If the calculated distance is less than the threshold value, it is classified as a violation and a red bounding box is marked and the violation count is incremented. Else, there is no violation detected, and a green bounding box is marked.

<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/social-1.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/social-2.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Images are taken from the project demo.
</div>

Codebase: <a href="https://github.com/hoplite2k/social-distancing">https://github.com/hoplite2k/social-distancing</a>
