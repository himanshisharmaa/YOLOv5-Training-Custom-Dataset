# YOLOv5-Training-Custom-Dataset
This repo is about training the custom vehicle dataset that has been taken from Kaggle. The training has been done using google colab. The repo contains:
- vehicle dataset with structured directories
- "custom_data.yaml" file which contains the path to the training dataset
- "YOLOv5_custom_dataset.ipynb" is the notebook containing the commanda and code for training the data.
- "videos" folder containing the videos for testing.
- "Custom_YOLOWeights" are the weights from the training.
-  "Yolo_Outputs" are the inferencing outputs.
Link: https://www.kaggle.com/datasets/nadinpethiyagoda/vehicle-dataset-for-yolo


## clone the yolo github repository by running the following command:
     git clone https://github.com/ultralytics/yolov5.git

## create a custom_dataset.yaml file or edit the given yaml file like coco128.yaml to add the path of the training dataset

## install all the requirements:
      cd yolov5
      pip install -r requirements.txt

## train the dataset using the following command:
    python train.py --img 640 --batch 16 --epochs 100 --data data/custom_data.yaml --weights yolov5s.pt

## Perform the inferencing using following command:
    python detect.py --weights /content/drive/MyDrive/Vehicle/yolov5/runs/train/exp2/weights/best.pt --      img 640 --conf 0.25 --source /content/drive/MyDrive/Vehicle/example_01.jpg
     

  
