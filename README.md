# Object_Detection_Module
This module contains the "data", "names", and "cfg" files which were used to train the Yolov4 custom object detector on the Pascal VOC 2012 dataset. It also contains an overview of the object detection results.

We trained the Yolov4 object detector on the Pascal VOC 2012 dataset and used NVIDIA Container Toolkit (NCT) and Docker. The workflow of the model training is exhibited in Figure 1 below.

<p align="center">
  <img src="https://user-images.githubusercontent.com/13494311/185402589-f3c55db3-1a04-4bc2-ab78-23bc8e587452.png" alt="Yolo Docker flowchart" width=30% height=20%>
</p>

<p align = "center">
Fig. 1 - The workflow of Yolov4 object detection model training
</p>

We conducted three model trainings (T1, T2, T3). 

In T1, we chose to train the model on 4 out of the 20 classes of the Pascal VOC dataset, namely, bus, car, motorbike, and person which are relevant to an IoV system for a quicker training. For this purpose, we removed the irrelevant classes from the Pascal dataset and generated our own dataset suitable for an IoV environment. T1 did not yield good results due to data imbalance: the number of images in the person class were significantly higher than the number of images in the other 3 classes.

In T2, we corrected this imbalance which resulted in good detection results. The link to this dataset is https://drive.google.com/drive/folders/123ooCUhg0jPyocsdesWnFJ5QBU8R-HfY

We could not achieve high mAP scores in T1 and T2. Hence, the final training (T3) was done on all the 20 classes of the Pascal dataset. 

Below are the object detection results on a few images for T1, T2, and T3. To view the results on more images, visit this link - https://drive.google.com/drive/folders/1y3aioIcrws8xNXrSyY5zQzhyXwGAwgSA

<p float="left">
  <img src="https://user-images.githubusercontent.com/13494311/185402972-c95ecbb8-ddee-444b-a019-e3341f255a54.jpg" width=32% />
  <img src="https://user-images.githubusercontent.com/13494311/185403048-cd958614-4cce-42c9-82f2-1f6cdbe7b9d9.jpg" width=32% /> 
  <img src="https://user-images.githubusercontent.com/13494311/185403138-009dda45-7f17-40f2-a90e-888ae1f8fecf.jpg" width=32% />
</p>

<p float="left">
  <img src="https://user-images.githubusercontent.com/13494311/185404254-fcab7e54-86ce-4038-bef6-3695a993ac84.jpg" width=32% />
  <img src="https://user-images.githubusercontent.com/13494311/185404367-894748d9-47ce-498a-8c31-2c575949c0ca.jpg" width=32% />
  <img src="https://user-images.githubusercontent.com/13494311/185404521-511e8792-7a4c-4842-8ebf-ae9ea4e0d029.jpg" width=32% />
</p>

<p align = "center">
Fig. 2 - Results of T1, T2, T3
</p>

We also trained a GAN model to obtain synthetic images. The workflow for the same is presented below in Figure 3.

<p align="center">
  <img src="https://user-images.githubusercontent.com/13494311/185407116-eb1a752a-576c-462a-99bd-f61f0bab5be5.jpg" alt="GAN_framework" width=30% height=20%>
</p>

<p align = "center">
Fig. 3 - The workflow of GAN model training
</p>

We performed daytime to nighttime image translation using GAN. The results are shown below. For more results, visit this link - https://drive.google.com/drive/folders/1bpPX3Ru812ef1I4SWytAxBjk1SQvbiFw

<p float="left">
  <img src="https://user-images.githubusercontent.com/13494311/185407664-5dd1ffc0-a1e8-4373-bcde-ba5dabaa4e6b.png" alt="Img1_day" width=32% />
  <img src="https://user-images.githubusercontent.com/13494311/185407722-dc8be53c-ac2f-47a4-80d5-5c20dc745a90.png" alt="Img1_night" width=32% />
</p>

<p float="left">
  <img src="https://user-images.githubusercontent.com/13494311/185407778-684d0d4b-d663-43ae-83e7-2b17d3bfed70.png" alt="Img2_day" width=32% />
  <img src="https://user-images.githubusercontent.com/13494311/185407840-7158e356-7162-47fb-ab33-653de74e5335.png" alt="Img2_night" width=32% />
</p>

<p align = "center">
Fig. 4 - Results of GAN
</p>
