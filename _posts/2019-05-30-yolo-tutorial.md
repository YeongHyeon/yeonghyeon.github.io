---
layout: post
categories: posts
title: You only look once (YOLO) - Real-Time Object Detection Tutorial
tags: [YOLO, deep-learning, object-detection]
date-string: MAY 30, 2019
---

# IN PROGRESS
This post covers the tutorial for using <a href="https://pjreddie.com/darknet/yolo/">YOLO</a>.  

### Download YOLO (Darknet)
``` sh
$ git clone https://github.com/pjreddie/darknet
$ cd darknet
```

### Makefile
First, you should adjust the setting of 'Makefile'  
```
# If you have GPU and GPU driver is installed, set this option as GPU=1
# Also, set other options as 1 if you already prepared.
GPU    = 0
CUDNN  = 0
OPENCV = 0
OPENMP = 0
DEBUG  = 0
```
Then, use ```make``` command to make environment.  
``` sh
$ make

gcc -Iinclude/ -Isrc/ -DGPU -I/usr/local/cuda/include/ -Wall -Wno-unused-result -Wno-unknown-pragmas -Wfatal-errors -fPIC -Ofast -DGPU -c ./src/gemm.c -o obj/gemm.o
gcc -Iinclude/ -Isrc/ -DGPU -I/usr/local/cuda/include/ -Wall -Wno-unused-result -Wno-unknown-pragmas -Wfatal-errors -fPIC -Ofast -DGPU -c ./src/utils.c -o obj/utils.o
...
gcc -Iinclude/ -Isrc/ -DGPU -I/usr/local/cuda/include/ -Wall -Wno-unused-result -Wno-unknown-pragmas -Wfatal-errors -fPIC -Ofast -DGPU obj/captcha.o obj/lsd.o obj/super.o obj/art.o obj/tag.o obj/cifar.o obj/go.o obj/rnn.o obj/segmenter.o obj/regressor.o obj/classifier.o obj/coco.o obj/yolo.o obj/detector.o obj/nightmare.o obj/instance-segmenter.o obj/darknet.o libdarknet.a -o darknet -lm -pthread -L/usr/local/cuda/lib64 -lcuda -lcudart -lcublas -lcurand -lstdc++ libdarknet.a
```

### Dataset
Construct dataset as <a href="http://host.robots.ox.ac.uk/pascal/VOC/">PASCAL VOC</a> form.  
```
Dataset
└─ Set Name
   ├─ Annotations
   │   └─ 1.xml, 2.xml, ... n.xml
   ├─ ImageSets
   │   └─ Main
   │       └─ train.xml, val.xml, test.xml
   ├─ JPEGImages
   │   └─ 1.jpg, 2.jpg, ... n.jpg
   ├─ labels
   │   └─ 1.txt, 2.txt, ... n.txt
   └─ Originals
       └─ 1.jpg, 2.jpg, ... n.jpg
```

You can achieve 'labels' directory of above structure by processing the dataset using following python script.  
``` sh
$ wget https://pjreddie.com/media/files/voc_label.py
$ python voc_label.py
```

However, you can manually construct 'labels' directory as following form.
```
# class number, center x of ROI, center y of ROI, width, height
# All values are provided with ratio form
# 0             0.63             0.43             0.21   0.39
# If you have multiple ROI in one image, list it sequentially.
0 0.63 0.43 0.21 0.39
```
