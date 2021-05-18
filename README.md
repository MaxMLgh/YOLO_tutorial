# Yolo tutorial
This is the code i used in my tutorial[yt link] of Yolo algorithm.

You can manipulate live thresholds(confidence-CONF, intersection of union-IOU) and accesories(anchor boxes, grids) using keyboard on image and see how it affects detection.
Keybord keys:
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
- '[' - substract 32 pixels to width
- ']' - add 32 pixels to width
- 't' - show class and probability on box ON/OFF
- 'T' - show text on the left

**If you'll click capital letter(left SHIFT + letter) gain/loss will be 0.1**

# Demo of keyboard stearing

![demo(1)](https://user-images.githubusercontent.com/73268650/114053923-acb1a280-988f-11eb-9bd4-2f2addaf8488.gif)




You can run detection on:
- images and videos from your pc/laptop
- directly from camera
- from most of images on the web just by passing the link of them.

You can comapre 4 algorithms on different input sizes(320, 416(most popular), 620, any integer multiple of 32):
- Yolov3
- Yolov3-tiny
- Yolov4
- Yolov4-tiny


# Instalation
First clone this repository using git 

``` bash
git clone https://github.com/jakub7535/yolo_tutorial.git
```
or simply  download and unpack the ZIP file(change folder name from 'yolo_tutorial-master' to 'yolo_tutorial' for convenience.
![image](https://user-images.githubusercontent.com/73268650/114109329-5b2c0680-98d5-11eb-8e7d-9f4711754fba.png)

Then enter the repository:

![image](https://user-images.githubusercontent.com/73268650/114109278-3f286500-98d5-11eb-8eeb-1990952282f0.png)

Installing using conda(recomended)

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
Make sure you are in yolo_tutorial repository (and your venv yolo_tutorial is activated for anaconda instalation). Type 'jupyter notebook' in cmd and notebook will open in your browser. You can run cells using Shift+Enter. If you want to use camera detection make sure you have it pluged in.
