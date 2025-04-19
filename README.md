# 2Dto3D-Golden-Ratio
2D to 3D Face Reconstruction & Beautification - Installation Guide
==================================================================
0. Install the main files and model from MY DRIVE
----------------------
https://drive.google.com/drive/folders/16_YdP-x4mpGSavLmAwsJx2avdyB2ja0N?usp=sharing

1. Install Required Python Packages
-----------------------------------
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
pip install numpy opencv-python matplotlib scikit-image imageio tqdm scipy tensorboardX
pip install yacs easydict ninja trimesh dominate pandas
pip install mediapipe==0.10.5

2. Install nvdiffrast
---------------------
git clone https://github.com/NVlabs/nvdiffrast.git
cd nvdiffrast
pip install .
cd ..

3. Clone insightface & Copy arcface_torch
-----------------------------------------
git clone https://github.com/deepinsight/insightface.git
cp -r ./insightface/recognition/arcface_torch ./Deep3DFaceRecon_pytorch/models/


4. Patch preprocess.py
------------------------------------
sed -i 's/np.VisibleDeprecationWarning/DeprecationWarning/' ./Deep3DFaceRecon_pytorch/util/preprocess.py

5. Extra Files (Google Drive/Colab Links)
-----------------------------------------
Pretrained Model (epoch_20.pth): 
https://drive.google.com/drive/folders/1liaIxn9smpudjjqMaWWRpP0mXRW_qRPP

BFM_Fitting.zip: 
https://drive.google.com/uc?id=1N2zU3xS_lAGAjVjGIMWdv-pS4XV_eogd

Colab Notebook: 
https://colab.research.google.com/drive/1oiiSdFMGstimV3irJXt0MqZ4CKBU2Zy7?usp=sharing

-----------------------------------------
- Run all commands sequentially.


