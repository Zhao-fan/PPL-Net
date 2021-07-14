# JPS-Net

## Requirement
python 3.7

pytorch>=1.5

torchvision>=0.6

opencv-python>=4.1

## Datatsets

Download datatsets for FGVC (e.g. CUB-200-2011, Standford Cars, FGVC-Aircraft, etc) and organize the structure as follows:

>dataset

>>train
>>>class_001
>>>>1.jpg
>>>>2.jpg
>>>>...
>>>class_002
>>>>1.jpg
>>>>2.jpg
>>>>...
>>>...

>>test
>>>class_001
>>>>1.jpg
>>>>2.jpg
>>>>...
>>>class_002
>>>>1.jpg
>>>>2.jpg
>>>>...
>>>...
    
## Performance
PyTorch experiments were done on two Titan V GPU (batch_size = 16).

Dataset  |  Object  |  Category  |  Train  |  Test  |  Accuracy
------  |  ------  |  --------|  ---------|  ------|  ------
CUB-200-2011  |  Bird  |  200  |  5994  |  5794  |  89.7
Stanford Cars  |  Car  |  196  |  8144  |  8041  |  95.3
FGVC-Aircraft  |  Aircraft  |  100  |  6667 |  3333  |  93.8

## Visualization

