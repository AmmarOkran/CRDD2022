# crddc2022
Crowdsensing-based Road Damage Detection Challenge (CRDDC2022)


# Crowdsensing-based road damage detection challange 2022 IRCV-URV submission

This repository contains source code and trained models for [Crowdsensing-based Road Damage Detection and Classification Challenge](https://crddc2022.sekilab.global/overview/) that was held as part of 2022 IEEE Big Data conference.

## Submission

All the trained models can be downloaded from [here](https://drive.google.com/drive/folders/1NO5Svrj5wY0lpe3xSKqZGGBJFsI-YLHW?usp=sharing).

### Training

### Inference

1. Download weights from [trained models](https://drive.google.com/drive/folders/1NO5Svrj5wY0lpe3xSKqZGGBJFsI-YLHW?usp=sharing).

2. Go to `yolov7` directory
    ```Shell
    cd yolov7
    ```

3. Start the inference:

#### - For all countries
```Shell
    # inference using ensemble model for all countries test dataset
    python detect.py --weights trined_models_paths --img 832 --source path-to-all-countries-test-dataset --conf-thres 0.32 --iou-thres 0.9999 --agnostic-nms --augment --cntry All_countries
```

#### - India
```Shell
    # inference using ensemble model for India test dataset
    python detect.py --weights trined_models_paths --img 832 --source path-to-India-test-dataset --conf-thres 0.30 --iou-thres 0.9999 --agnostic-nms --augment --cntry India
```

#### - Japan
```Shell
    # inference using ensemble model for Japan test dataset
    python detect.py --weights trined_models_paths --img 832 --source path-to-Japan-test-dataset --conf-thres 0.30 --iou-thres 0.9999 --agnostic-nms --augment --cntry Japan
```

#### - Norway
```Shell
    # inference using ensemble model for Norway test dataset
    python detect.py --weights trined_models_paths --img 1664 --source path-to-Norway-test-dataset --conf-thres 0.20 --iou-thres 0.9999 --agnostic-nms --augment --cntry Norway
```

#### - United States
```Shell
    # inference using ensemble model for United States test dataset
    python detect.py --weights trined_models_paths --img 832 --source path-to-United_States-test-dataset --conf-thres 0.30 --iou-thres 0.9999 --agnostic-nms --augment --cntry United_States
```

## All ensemble models
| Ensemble model | Yolov7(trained from scratch) | Yolov7(fine-tuned) | Yolov7x(fine-tuned) | Yolov7x with ASPP | Yolov7-e6e(multi-scale) | Yolov7-e6e(All Countries) | Yolov7-e6e(Just Norway) |
|----------------|------------------------------|--------------------|---------------------|-------------------|-------------------------|--------------------------|-------------------------|
| Model 1 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |                |                         |                       |                          |
| Model 2 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |                  | :heavy_check_mark: |                         |                       |                          |
| Model 3 |                    |                    |                    |                  | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |





## Performance on CRDDC2022 test datasets


| Ensemble model | Country test dataset | F1-score |
|----------------|--------------------- |----------|
| Model 1 | All countries | **0.726267534039815** |
| Model 1 | Japan | **0.734582093871738** |
| Model 1 | India | **0.517735600502415** |
| Model 3 | Norway | **0.498392411476723** |
| Model 2 | United States | **0.778857992128306** |


