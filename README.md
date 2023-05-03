# CS4803-Novel-Object-Tracking

## Datasets

- Need For Speed Object Tracking Dataset (NFS): [Dataset Link](https://ci2cv.net/nfs/index.html)

- Using the "Get_NFS.sh" script, you can download certain parts of the dataset. The following were used:
    - basketball_1
    - basketball_2
    - basketball_3
    - basketball_6
    - basketball_player
    - basketball_player_2
    - Gymnastics
    - running_2
    - soccer_player_3
    - walking
    - walking_3


## File Structure

data: Contains both the raw NFS and the saved preprocessed data by running dataloader.py
models: Contains the classes and functions for various types of models (The main model is in models/CNN.py)

out: Output directory for model outputs and media

saved_models: Contains the state dicts of the trained models

dataloader.py: Contains the functions for loading the data and preprocessing it

train.ipynb: Contains the code for training the model

test_yolo.ipynb: Contains the code for testing the model

## Usage

1. Install the dependencies
    - `pip install -r requirements.txt`
2. Download the dataset from the link above.
3. Unzip the dataset.
4. Run the dataloader.py script to generate the preprocessed data.
    - Modify the file string at the end of the script to point to the correct dataset.
    - Comment out the relevant scripts in the main script to produce the dataset
5. Train the CNNForecaster model in the train.py jupyter notebook.
    - Modify the file strings in the notebook to point to the correct dataset.
6. Run the test_yolo.ipynb notebook to test the model.
    - Modify the file strings in the notebook to point to the correct dataset.
7. Video output will be saved to the "out" directory.

## Results - Video Output

The following video files are produced by the test_yolo.ipynb notebook

- [out/basketball_yolo.mp4](https://drive.google.com/drive/folders/19yZ8e0Fj96vfiS7mFaATcPcalCm3angq?usp=sharing)
    - Green Box in the beginning represents the inital series generated by YOLO
    - Red box is the continual object tracking using our algorithm