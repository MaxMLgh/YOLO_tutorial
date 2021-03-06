# Yolo tutorial
This is the code i used in my tutorial of Yolo algorithm.  
Link to **YouTube** video:    
https://www.youtube.com/watch?v=MKF1NHGgFfk  
The head of Yolo v3, v4, tiny algorithms works roughly the same, the main change is in the 'back-bone' which is feature extractor.  
So experiment on them to find which one works the best for you.  
You can manipulate live thresholds(confidence-CONF, intersection of union-IOU) and accessories(anchor boxes, grids) using keyboard on the image and see how it affects detection.
Keyboard keys:
- 'w'/'W' - IOU + 0.01/0.1
- 's'/'S' - IOU - 0.01/0.1
- 'd'/'D' - CONF + 0.01/0.1
- 'a'/'A' - CONF - 0.01/0.1
- 'b' - show/hide anchor boxes ON/OFF
- 'g' - show hide grid and center of object ON/OFF
- 'space' - pause/unpause
- 'v' - record video ON/OFF
- 'p' - screen shot
- 'r' - image ratio ON/OFF
- '3' - yolov3
- '4' - yolov4
- '#' - yolov3-tiny
- '$' - yolov4-tiny
- '[' - subtract 32 pixels to the width
- ']' - add 32 pixels to the width
- 't' - show class and probability on box ON/OFF
- 'T' - show text on the left

**If you'll click capital letter(left SHIFT + letter) gain/loss will be 0.1**

# Demo of the keyboard steering

![demo(1)](https://user-images.githubusercontent.com/73268650/114053923-acb1a280-988f-11eb-9bd4-2f2addaf8488.gif)




You can run detection on:
- images and videos from your pc/laptop
- directly from camera
- from most of the images on the web just by passing the link of them.

You can compare 4 algorithms on different input sizes(320, 416(most popular), 620, any integer multiple of 32):
- Yolov3
- Yolov3-tiny
- Yolov4
- Yolov4-tiny
# Google Colab notebook 
If you first want to give it a try before installing check the Google colab version. 
You can do there everything that you could do on your machine but only on image from the web and without the keyboard commands, you need to initialize instance of class Detetcion with right parameters.  
Link to colab notebook:  
https://colab.research.google.com/github/MaxMLgh/YOLO_tutorial/blob/master/Google_Colab_Yolo_Tutorial.ipynb
![image](https://user-images.githubusercontent.com/84282532/119281270-65ac2080-bc35-11eb-903d-4de313688106.png)


# Instalation on your machine
First clone this repository using git 

``` bash
git clone https://github.com/MaxMLgh/YOLO_tutorial.git
```
Or simply  download and unpack the ZIP file(change folder name from 'yolo_tutorial-master' to 'yolo_tutorial' for convenience.
Then enter the repository.

Installing using conda(recommended)

``` bash
conda create --name yolo_tutorial python=3.8
conda activate yolo_tutorial
pip install opencv-python==4.5.1.48 numpy==1.19.2 pafy youtube-dl jupyter
python -m ipykernel install --user --name yolo_tutorial --display-name "yolo_tutorial"
```
Installing using pip

``` bash
pip install opencv-python==4.5.1.48 numpy==1.19.2 jupyter pafy youtube-dl
```
# Links to weights
In order to run detection you must download weights you want to use for neural network(click on the name of the model below) and place them in folder **'net'** in the repository. 
**IMPORTANT**, make sure the names are exactly the same as in the images below(eg. yolov4.weights, not yolov4(1).weights)
![image](https://user-images.githubusercontent.com/73268650/114060309-8989f180-9895-11eb-8c42-2f50958580f8.png)
![image](https://user-images.githubusercontent.com/73268650/114060449-ade5ce00-9895-11eb-9ea4-7d3da5da6396.png)


- [yolov3](https://pjreddie.com/media/files/yolov3.weights) (242MB)
- [yolov3-tiny](https://pjreddie.com/media/files/yolov3-tiny.weights) (35MB)
- [yolov4](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights) (252MB)
- [yolov4-tiny](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4-tiny.weights) (24MB)(already in the folder 'net')

# How to run
Make sure you are the in yolo_tutorial repository (and your venv yolo_tutorial is activated for anaconda installation). Type 'jupyter notebook' in cmd and notebook will open in your browser. You can run cells using Shift+Enter. If you want to use camera detection make sure you have it plugged in.
