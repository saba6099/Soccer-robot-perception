# Soccer-robot-perception-model


Authors: Saba Khan, [Tejas Morbagal Harish](https://github.com/TejasMorbagal/)

Repository of the final Project implemented as a part of CudaVision Lab at University of Bonn (WS19).
Implemented the model described in the [Paper](https://www.researchgate.net/publication/337702097_RoboCup_2019_AdultSize_Winner_NimbRo_Deep_Learning_Perception_In-Walk_Kick_Push_Recovery_and_Team_Play_Capabilities) for detecting ball, goalposts, and robots as well as for pixel-wise segmentation of filed and lines.

For further details please read the [Project Report](https://github.com/saba6099/Soccer-robot-perception-model/blob/master/Final_report.pdf).

A unified deep-learning network is implemented based on the encoder-decoder approach to perform object detection and pixel-wise classification. The network architecture is as shown below:

![](https://github.com/saba6099/Soccer-robot-perception-model/blob/master/Fig%202.png "Architecture")

For image detection, we applied some data augmentation methods like horizontal flip and slight color jitter to introduce variability in the data. Further, the normalization of the dataset is performed with the same values used in the Resnet18 pre-trained network. Furthermore, three heat-maps corresponding to three output channels are generated for robot, goalposts and ball. The figure shows the corresponding heatmaps.
![heatmaps](https://github.com/saba6099/Soccer-robot-perception-model/blob/master/Output%20Images/Fig%201.1.png)

 To test the segmentation head, we visualize the output of the model for several images as shown below.	We also calculate pixel accuracy and IOU for test data.

![Segmentation](https://github.com/saba6099/Soccer-robot-perception-model/blob/master/Output%20Images/Fig%204.1.png)

