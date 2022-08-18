# Object_Detection_Module
This module contains the "data", "names", and "cfg" files which were used to train the Yolov4 custom object detector on the Pascal VOC 2012 dataset. It also contains an overview of the object detection results.

We trained the Yolov4 object detector on the Pascal VOC 2012 dataset and used NVIDIA Container Toolkit (NCT) and Docker. The workflow of the model training is exhibited in Figure 1 below.

<img src="https://user-images.githubusercontent.com/13494311/185402589-f3c55db3-1a04-4bc2-ab78-23bc8e587452.png" alt="Yolo Docker flowchart" width=49% height=49%>
<p align = "left">
Fig. 1 - The workflow of Yolov4 object detection model training
</p>

We conducted three model trainings (T1, T2, T3). 

In T1, we chose to train the model on 4 out of the 20 classes of the Pascal VOC dataset, namely, bus, car, motorbike, and person which are relevant to an IoV system for a quicker training. For this purpose, we removed the irrelevant classes from the Pascal dataset and generated our own dataset suitable for an IoV environment. T1 did not yield good results due to data imbalance: the number of images in the person class were significantly higher than the number of images in the other 3 classes.

In T2, we corrected this imbalance which resulted in good detection results. The link to this dataset is https://drive.google.com/drive/folders/123ooCUhg0jPyocsdesWnFJ5QBU8R-HfY

We could not achieve high mAP scores in T1 and T2. Hence, the final training (T3) was done on all the 20 classes of the Pascal dataset. 

Below are the object detection results on a few images for T1, T2, and T3.

<p float="left">
  <img src="https://user-images.githubusercontent.com/13494311/185402972-c95ecbb8-ddee-444b-a019-e3341f255a54.jpg" width=40% />
  <img src="https://user-images.githubusercontent.com/13494311/185403048-cd958614-4cce-42c9-82f2-1f6cdbe7b9d9.jpg" width=40% /> 
  <img src="https://user-images.githubusercontent.com/13494311/185403138-009dda45-7f17-40f2-a90e-888ae1f8fecf.jpg" width=40% />
</p>
