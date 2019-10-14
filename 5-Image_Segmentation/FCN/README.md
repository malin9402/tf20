## FCN: Fully Convolutional Networks for Semantic Segmentation
--------------------
 [This paper](https://arxiv.org/abs/1411.4038) shows that convolutional networks by themselves, trained end-to-end, pixels-to-pixels, exceed the state-of-the-art in semantic segmentation. This repo adapts vgg16 networks into fully convolutional networks and transfer their learned representations by fine-tuning to the segmentation task on PASCAL VOC2012 dataset. 

## Train PASCAL VOC2012
--------------------
Download VOC PASCAL trainval and test data. 
```bashrc
$ wget http://host.robots.ox.ac.uk/pascal/VOC/voc2007/VOCtrainval_06-Nov-2007.tar
$ wget http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar
$ wget http://host.robots.ox.ac.uk/pascal/VOC/voc2007/VOCtest_06-Nov-2007.tar
```
Extract all of these tars into one directory and rename them, which should have the following basic structure.
```bashrc
VOC           # path:  /home/yang/test/VOC/
├── test
|    └──VOCdevkit
|       └──VOC2007 (from VOCtest_06-Nov-2007.tar)
└── train
     └──VOCdevkit
             └──VOC2007 (from VOCtrainval_06-Nov-2007.tar)
                     └──VOC2012 (from VOCtrainval_11-May-2012.tar)
```
Then you need to make some transformation.
```bashrc
$ python parser_voc.py --data_path /home/yang/test/VOC
```

|![image](https://user-images.githubusercontent.com/30433053/66732790-d4d56680-ee8f-11e9-9120-07b0e8aa53d4.jpg)|![image](https://user-images.githubusercontent.com/30433053/66732790-d4d56680-ee8f-11e9-9120-07b0e8aa53d4.jpg)|![image](https://user-images.githubusercontent.com/30433053/66732795-da32b100-ee8f-11e9-9d85-f0ddba7a3ab1.jpg)|
|---|---|:---:|
|![image](https://user-images.githubusercontent.com/30433053/66732795-da32b100-ee8f-11e9-9d85-f0ddba7a3ab1.jpg)|![weibo-logo](https://github.com/YunYang1994/SphereFace/blob/master/image/original_softmax.png)|![image](https://user-images.githubusercontent.com/30433053/66732795-da32b100-ee8f-11e9-9d85-f0ddba7a3ab1.jpg)|
