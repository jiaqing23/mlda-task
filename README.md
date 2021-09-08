# MLDA Task

## File structure
```
Project
│   README.md
│   train.csv
│   inference.ipynb
│   prepare.ipynb
│   train.csv
│   requirements.txt
│   
└───robot_camera
│   │   robot_camera_0.jpg
│   │   ...
│   
└───robot_camera_annotation
│   │   robot_camera_0.xml
│   │   ...
```

## Dependencies
```
pip install -r requirements.txt
```
> requirements.txt is generate from Kaggle environment by running pip freeze, might contain much more package than needed.

## Preprocess
This is to convert XML labels to Pandas DataFrame. Just change the `raw_labels_root` as path of folder of xml labels (`robot_camera_annotation`) in first block in `prepare.ipynb` and run the whole notebook. It will generate `train.csv`.


## Train
1. Change `DIR_INPUT` and `DIR_TRAIN` as path of root folder of project and folder of images.
2. Run whole notebook.

## Inference
1. Change `WEIGHTS_FILE` to path of pretrained weights file.
2. Change `DIR_IMAGE` as path of images to inference.
3. Run whole notebook, it will generate output to `output.csv`.
