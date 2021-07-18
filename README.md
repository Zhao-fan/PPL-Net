# JPS-Net

Code release for Fine-grained Visual Classification by Progressive Training via Jigsaw Puzzle Solver.

## Abstract
Fine-grained visual classification remains a challenging task due to small inter-class differences and large intra-class differences. Classifying subclasses of objects from a superclass is highly dependent on finding discriminative feature representations. Recent work has started to focus on using image patches to process the original image instead to learn feature representations with different size granularity. However, these approaches rarely pay attention to the impact of the location information of each patch on the classification performance. To solve the above problem, we propose a progressively trained Jigsaw Puzzle Solver network (JPS-Net). Firstly, we use a simple jigsaw puzzle generator to generate image patches at different levels of granularity. And each patch is shuffled to get a shuffled version of the image. Then, in order to fuse feature information of different granularity for classification, we adopt an progressive training strategy. Specifically, for different steps, we add different granularity levels of the shuffled versions of the images as the input. And we select the output feature maps of different intermediate stages of the backbone network. Thus, we obtain feature representations with different granularity levels. The final prediction score is the sum of the prediction scores of each step. Finally, to explore the location information of the image patches at different granularities, we introduce a Jigsaw Puzzle Solver module. We apply the sinkhorn operator to the feature maps extracted by the backbone network to obtain a double random matrix. This double random matrix reflects the most likely global assignment of the output patches. Experiments on three standard fine-grained classification datasets (CUB-200-2011, Stanford Cars, FGCV-Aircraft) show that the performance of our method exceeds that of most methods.

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

Dataset  |  Object  |  Category  |  Train  |  Test  |  Accuracy  
------  |  ------  |  --------|  ---------|  ------|  ------ 
CUB-200-2011  |  Bird  |  200  |  5994  |  5794  |  89.7  
Stanford Cars  |  Car  |  196  |  8144  |  8041  |  95.3  
FGVC-Aircraft  |  Aircraft  |  100  |  6667 |  3333  |  93.8 

## Visualization

Code in Gard-CAM.py helps generate visualization.

![image](https://github.com/Zhao-fan/JPS-Net/blob/main/images/vis.png)

## Acknowledgement

Many thanks to [PMG-Progressive-Multi-Granularity-Training](https://github.com/PRIS-CV/PMG-Progressive-Multi-Granularity-Training) of [Fine-Grained Visual Classiﬁcation via Progressive Multi-Granularity Training of Jigsaw Patches](https://arxiv.org/abs/2003.03836).

