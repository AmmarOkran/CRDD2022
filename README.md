# crddc2022
Crowdsensing-based Road Damage Detection Challenge (CRDDC2022)


# Crowdsensing-based road damage detection challange 2022 IRCV-URV submission

This repository contains source code and trained models for [Crowdsensing-based Road Damage Detection and Classification Challenge](https://crddc2022.sekilab.global/overview/) that was held as part of 2022 IEEE Big Data conference.

## Submission

All the trained models can be downloaded from [here](https://drive.google.com/drive/folders/1NO5Svrj5wY0lpe3xSKqZGGBJFsI-YLHW?usp=sharing).


### Inference

1. Download weights from [trained models](https://drive.google.com/drive/folders/1NO5Svrj5wY0lpe3xSKqZGGBJFsI-YLHW?usp=sharing).

2. Go to `yolov7` directory
    ```Shell
    cd yolov7
    ```

3. Start the inference:

### - For all countries
```Shell
    # inference using ensemble model for all countries test dataset
    python detect.py --weights trined_models paths --img 640 --source path-to-all-countries-test-dataset --conf-thres 0.32 --iou-thres 0.9999 --agnostic-nms --augment --cntry All_countries
```

### - India
```Shell
    # inference using ensemble model for all countries test dataset
    python detect.py --weights trined_models paths --img 640 --source path-to-India-test-dataset --conf-thres 0.32 --iou-thres 0.9999 --agnostic-nms --augment --cntry India
```

### - Japan
```Shell
    # inference using ensemble model for all countries test dataset
    python detect.py --weights trined_models paths --img 640 --source path-to-Japan-test-dataset --conf-thres 0.32 --iou-thres 0.9999 --agnostic-nms --augment --cntry Japan
```

### - Norway
```Shell
    # inference using ensemble model for all countries test dataset
    python detect.py --weights trined_models paths --img 640 --source path-to-Norway-test-dataset --conf-thres 0.32 --iou-thres 0.9999 --agnostic-nms --augment --cntry Norway
```

### - United States
```Shell
    # inference using ensemble model for all countries test dataset
    python detect.py --weights trined_models paths --img 640 --source path-to-United_States-test-dataset --conf-thres 0.32 --iou-thres 0.9999 --agnostic-nms --augment --cntry United_States
```