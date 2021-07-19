# JPS-Net

Code release for Fine-grained Visual Classification by Progressive Training via Jigsaw Puzzle Solver.

## Abstract


## Requirement
python 3.7

pytorch>=1.5

torchvision>=0.6

opencv-python>=4.1

## Datatsets

Download datatsets for FGVC (e.g. CUB-200-2011, Standford Cars, FGVC-Aircraft, etc) and organize the structure as follows:

>dataset

>>--train
>>>---class_001
>>>>----1.jpg

>>>>----2.jpg

>>>>----...

>>>---class_002

>>>>----1.jpg

>>>>----2.jpg

>>>>----...

>>>---...

>>--test
>>>---class_001
>>>>----1.jpg

>>>>----2.jpg

>>>>----...

>>>---class_002

>>>>----1.jpg

>>>>----2.jpg

>>>>----...

>>>---...


## Performance 
PyTorch experiments were done on two Titan V GPU (batch_size = 16). Download the trained model, the extraction code is 1234.

Dataset  |  Object  |  Category  |  Train  |  Test  |  Accuracy |  model  
------  |  ------  |  --------|  ---------|  ------|  ------ |  --------
CUB-200-2011  |  Bird  |  200  |  5994  |  5794  |  89.7  |  [bird_model](https://pan.baidu.com/s/1uxCJsk2lvFlN9fUQF5EoUA)
Stanford Cars  |  Car  |  196  |  8144  |  8041  |  95.3  |  [car_model](https://pan.baidu.com/s/1wuf44hIBCJdN1PMUir1y9Q)
FGVC-Aircraft  |  Aircraft  |  100  |  6667 |  3333  |  93.8  | [aircraft_model](https://pan.baidu.com/s/1tMwOqES_fSLWytS0fLBCUw)

## Visualization

Code in Gard-CAM.py helps generate visualization.

![image](https://github.com/Zhao-fan/JPS-Net/blob/main/images/vis.png)

## Acknowledgement

Many thanks to [PMG-Progressive-Multi-Granularity-Training](https://github.com/PRIS-CV/PMG-Progressive-Multi-Granularity-Training) of [Fine-Grained Visual Classiﬁcation via Progressive Multi-Granularity Training of Jigsaw Patches](https://arxiv.org/abs/2003.03836).

