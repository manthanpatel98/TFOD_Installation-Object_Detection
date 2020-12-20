# TFOD_Installation-Object_Detection
Installation of TFOD and Performing Object Detection.

## **TFOD Installation:**
**1> Download official Github repo of TF-1 OD:**  https://github.com/tensorflow/models/tree/v1.13.0 **& Extract it in a folder.**

**2> Create Virtual Environment in [Anaconda](https://www.anaconda.com/) with python=3.6:**   conda create -n tfod python=3.6

**3> Activate Environment:**  conda activate tfod

**4> Install required libraries for tensorflow:** 

pip install pillow lxml Cython contextlib2 jupyter matplotlib pandas opencv-python tensorflow==1.14.0


**5> Keep the "research" folder (consider "research" folder as a parent directory) from "models" folder and delete other folders**

**6> In Anaconda Prompt, Go to "research" folder & Install Object Detection Library with file setup.py:** python setup.py install 

**7> Converting some .proto format files at [\models\research\object_detection\protos] to .py format:** 
      
   *  **Install protobuf library:** conda install -c anaconda protobuf
   
   *  **Converting .proto files to .py format files:**
            
         **For Linux / Mac / Windows :** protoc object_detection/protos/*.proto --python_out=.
         
         
 **8> Copy "object_detection_tutorial.ipynb" file from "object_detection" folder to "research" folder, then run jupyter notebook from "research" folder, and Open "object_detection_tutorial.ipynb".**
 
 **9> In "object_detection_tutorial.ipynb", Under "object Detection imports" cell, make a change in "from utils" to "from object_detection.utils" to avoid import error.**
 
 
