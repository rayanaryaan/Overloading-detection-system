# Overloading-detection-system

Final project for the Building AI course

## Summary

Overloading Detection System can be used to raise warning when system's bearing capacity exceeds. It usages pre-trained models to detect objects, age and gender.

## Background

There are lot of incidents happened due to overloading like 
* Bridge crash due to huge crowd which crosses total bearing load
* Passenger overloading on public transports i.e. bus, trains etc
* Huge crowd within confined space

Implementation recognize different objects along with human faces and predict total weights of all humans. Ability to raise overload warning.


## How is it used?
Install all dependent package using the following commands:
<pre><code>pip install -r requirements.txt </code></pre>
## dlib package installation
Open conda command prompt and install dlib using the following command:
<pre><code>conda install -c conda-forge dlib</code></pre>
Note: In case of permission issue, use command prompt with Admin permission.

## How to run:
The code is tested in python 3.7.8. 

Use anaconda command prompt and execute the following command:
<pre><code>jupyter notebook </code></pre>

Lunch notebook and run kernel.


## Data sources and AI methods

Object Detection Model
- **YOLO:** 
    - git clone https://github.com/pjreddie/darknet
    - wget https://pjreddie.com/media/files/yolov3.weights
    - Copy the followings:
        - **Models/yolov3.weights**
        - **cfg/yolov3.cfg**
        - **data/coco.names**

- **Age Net Model:** 
    - Config: **Models/age_deploy.prototxt**
    - Model: **Models/age_net.caffemodel**
    - Download link: https://drive.google.com/file/d/1yy_poZSFAPKi0y2e2yj9XDe1N8xXYuKB/view
- **Gender Net Model:** 
    - Config file: **Models/gender_deploy.prototxt**
        - Download link: https://drive.google.com/open?id=1AW3WduLk1haTVAxHOkVS_BEzel1WXQHP
    - Model: **Models/gender_net.caffemodel**
        -Download link: https://drive.google.com/open?id=1W_moLzMlGiELyPxWiYQJ9KFaXroQ_NFQ


## Challenges

False alarm may raise (false-positive case) and false negative cases may arise when system failed to recognized all objects. Following issues needs to be handled in efficient way in future:
* Recognizing age of detected human beings may not be accurate for every region which leads to following issues:
    * Total weight calculation
    * May lead to false notification. False-negative cases meeds to be handle efficiently.
* Total number of human object/gender detection for long distance camera feed may not be accurrate.


## What next?

Suggest for following improvements:
* Use deep neural network trained models to have better recognization of no of objects to reduce false-negative cases.
* Need to improve object recognization of long range videos/photos

## Acknowledgments
References:
- https://cloudxlab.com/blog/object-detection-yolo-and-python-pydarknet/
- https://github.com/juan-csv/Face_info
 

