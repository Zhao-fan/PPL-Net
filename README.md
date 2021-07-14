# JPS-Net

Code release for Fine-grained Visual Classification by Progressive Training via Jigsaw Puzzle Solver.

## Abstract
Fine-grained visual classification remains a challenging task due to small inter-class differences and large intra-class differences. Classifying subclasses of objects from a superclass is highly dependent on finding discriminative feature representations. Existing approaches mainly converge on using attention mechanisms or various granularity components to solve this problem. But no thought is given to the impact of positional information among various granularities on network performance. To solve the above problem, we propose a progressively trained Jigsaw Puzzle Solver network (JPS-Net). Specifically, based on a classical classification network, we introduce a Jigsaw Puzzle Solver module. The shuffled version of the image is used as the input to the network. A double random matrix is obtained as the replacement matrix by applying the sinkhorn operator to the feature maps extracted by the backbone network. This double random matrix reflects the most likely global assignment of the output patches. And then applying a permutation loss to the matrix is supervised. Experiments on three standard fine-grained classification datasets (CUB-200-2011, Stanford Cars, FGCV-Aircraft) show that the performance of our method exceeds that of most methods.

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


## Performance and Pre-trained models
PyTorch experiments were done on two Titan V GPU (batch_size = 16).

Dataset  |  Object  |  Category  |  Train  |  Test  |  Accuracy  |  Pre-trained models
------  |  ------  |  --------|  ---------|  ------|  ------  |  --------
CUB-200-2011  |  Bird  |  200  |  5994  |  5794  |  89.7  |  [CUB](G:\premodel\bird_gpu2_16\model.pth)
Stanford Cars  |  Car  |  196  |  8144  |  8041  |  95.3  |  [Car](G:\premodel\car\model.pth)
FGVC-Aircraft  |  Aircraft  |  100  |  6667 |  3333  |  93.8  |  [Air](G:\premodel\air\model.pth)

## Visualization

Code in Gard-CAM.py helps generate visualization.

![image](https://github.com/Zhao-fan/JPS-Net/blob/main/images/vis1.PNG)

