# Pedestrian Detection & Behaviour Classification 

## Model Components
This project involves developing a fully integrated system for pedestrian intent detection. The system consists of multiple components, each playing a specific role:  

- **YOLOv3 (Object Detection):** Identifies and detects pedestrians in an image or video frame.  
- **SORT (Object Tracking):** Tracks detected pedestrians across multiple frames and assigns unique IDs to maintain continuity.  
- **Spatio-Temporal DenseNet (Classification):** Utilizes the last 16 frames of a tracked pedestrian to predict their intent.  

## Repo contents
* `/data` - Consists file for class name
* `/SORT` - Additional file for SORT
* `/tf-pose-estimation` - Skeleton fitting algorithm files
* `/yolov3_tf2` - Yolov3 algorithm files
* `/yolov3_tf2.egg-info` - Yolov3 additional files
* `densenet_1.hdf5` - Weights for ST-DenseNet that uses original images
* `densenet_model.json` - Saved ST-DenseNet Model file in json format
* `LICENSE` - MIT License for this repo
* `mars-small128.pb` - Protocol buffer weight file for DeepSORT
* `pedestrian_inference.ipynb` - Google colab file for inferencing
* `README.md` - Instructions on how to use this repo
* `sortn.py` - SORT algorithm

# Running the Pedestrian Intent Detection Models on Google Colab  
The models were developed and executed using Google Colab, an online platform for running iPython notebooks. Each model has its dedicated Colab notebook. Follow the steps below to set up and run the notebooks:  

## Setup Instructions  
1. **Note**: The projects is compatabile with Google Colab Python version = 3.10
2. Open **pedestrian_inference.ipynb** in Google Colab.  
3. If the notebook is not editable, switch to **playground mode**. These steps are also outlined within each Colab notebook but are summarized here for convenience.  
4. Enable GPU acceleration for improved performance:  
   - Navigate to **Runtime** → **Change runtime type** → Select **GPU**.  
5. Clone the repository in a notebook cell:  
   ```bash
   !git clone https://github.com/AsangCode/Pedestrian_Behaviour_Prediction

6. Install the required dependencies by executing the following commands:

    ```bash
    !pip install tensorflow==2.15.1

7. Execute the remaining cells in the notebook using Shift + Enter, following the specific instructions for each model, and analyze the results.