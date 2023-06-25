# Crack Detection using YOLOv7
This repository contains Python notebook for training YOLOv7 network for a object detection task of cracks detection.

## Dataset
Datased used to train the network was provided as part of [ICUAS UAV Competition](http://www.uasconferences.com/2023_icuas/unmanned-aerial-vehicle-uav-competition/), and can be accesed from a [link](https://sites.google.com/view/retopercepcioncatec/datasets). The dataset consist out of 11 298 images containing cracks with labels written in YOLO labeling format.

## Usage
To use this notebook and train the YOLOv7 network, you need to download the dataset from a link.
Once the dataset is downloaded, make sure to change the dataset path variable in the notebook to match your own. From here, the notebook will take care of the rest. It will split the dataset, check if the data is split correctly, create the data.yaml file necessary for starting YOLOv7 training, and eventually start training.

## Results
The network was trained for 150 epochs with a batch size of 64 using default hyperparameters, and the results are shown in the table below:

| Metric       | Value  |
|--------------|--------|
| Precision    | 85.9%  |
| Recall       | 80.7%  |
| mAP@0.5      | 85.9%  |
| mAP@0.5:0.95 | 66.2%  |

The `precision` metric indicates the accuracy of the model in correctly identifying cracks, while `recall` represents the model's ability to detect all cracks in the dataset. The mean Average Precision (`mAP`) at different intersection over union (`IoU`) thresholds evaluates the model's performance across varying levels of overlap between predicted and ground truth bounding boxes.

Additionally, four graphs are included to visualize the training progress of the YOLOv7 model. These graphs show the progress of metrics throughout the training epochs.

<p align="center">
  <img src="https://github.com/AndroKatanec/Crack-Detection-using-YOLOv7/assets/73703833/4a321732-1a7b-49db-92b8-020c7e4a8969" width="700">
</p>

<p align="center">
  <img src="https://github.com/AndroKatanec/Crack-Detection-using-YOLOv7/assets/73703833/cd0a28ac-5a18-4a12-bebf-77e0a9ef5938" width="700">
</p>

<p align="center">
  <img src="https://github.com/AndroKatanec/Crack-Detection-using-YOLOv7/assets/73703833/7ac0e7c4-d415-4d4f-ad06-3dc187eda432" width="700">
</p>

<p align="center">
  <img src="https://github.com/AndroKatanec/Crack-Detection-using-YOLOv7/assets/73703833/496c3ab0-6f31-4f48-afab-ea613abc317e" width="700">
</p>



