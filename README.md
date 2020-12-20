# TFOD_Installation-Object_Detection
Installation of TFOD and Performing Object Detection.

<img src="https://github.com/manthanpatel98/TFOD_Installation-Object_Detection/blob/main/tfod_images/tensorflow.png" width="600">


## **TFOD Installation:**
**1> Download official Github repo of TF-1 OD:**  https://github.com/tensorflow/models/tree/v1.13.0 **& Extract it in a folder.**

**2> Create Virtual Environment in [Anaconda](https://www.anaconda.com/) with python=3.6:**   
                        
    conda create -n tfod python=3.6

**3> Activate Environment:**  
             
    conda activate tfod

**4> Install required libraries for tensorflow:** 

    pip install pillow lxml Cython contextlib2 jupyter matplotlib pandas opencv-python tensorflow==1.14.0


**5> Keep the "research" folder (consider "research" folder as a parent directory) from "models" folder and delete other folders**

**6> In Anaconda Prompt, Go to "research" folder & Install Object Detection Library with file setup.py:** 

      python setup.py install 

**7> Converting some .proto format files at [\models\research\object_detection\protos] to .py format:** 
      
   *  **Install protobuf library:** 
   
          conda install -c anaconda protobuf
   
   *  **Converting .proto files to .py format files:**
            
         **For Linux / Mac / Windows :** 
                 
          protoc object_detection/protos/*.proto --python_out=.
         
 ---
 
 ## **Object Detection:**
 
 **8> Copy "object_detection_tutorial.ipynb" file from "object_detection" folder [\research\object_detection] to "research" folder, then run jupyter notebook from "research" folder, and Open "object_detection_tutorial.ipynb".**
 
 **9> In "object_detection_tutorial.ipynb", There are 3 changes will be need as we have moved some files & folders locations:**
  *   **Under "object Detection imports" cell, make a change in "from utils" to "from object_detection.utils" to avoid import error.**
 
   <img src="https://github.com/manthanpatel98/TFOD_Installation-Object_Detection/blob/main/tfod_images/Screenshot%20(328).png" width="650">
 
  *   **Change path in PATH_TO_LABELS:**
 
  <img src="https://github.com/manthanpatel98/TFOD_Installation-Object_Detection/blob/main/tfod_images/Screenshot%20(329).png" width="650">
 
  *   **Change Under Detection PATH_TO_TEST_IMAGES_DIR:**
 
  <img src="https://github.com/manthanpatel98/TFOD_Installation-Object_Detection/blob/main/tfod_images/Screenshot%20(332).png" width="650">
 
## **Results:**

<img src="https://github.com/manthanpatel98/TFOD_Installation-Object_Detection/blob/main/tfod_images/tf1.png" width="600">

<img src="https://github.com/manthanpatel98/TFOD_Installation-Object_Detection/blob/main/tfod_images/tf2.png" width="600">
 
---

## **How to use another Model?**

*  **To add another model goto the [TensorFlow 1 Detection Model Zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md) & hover over the model name which will show model's exact name at the left bottom corner:**

<img src="https://github.com/manthanpatel98/TFOD_Installation-Object_Detection/blob/main/tfod_images/Screenshot%20(330).png" width="650">

*  **Change this at MODEL_NAME:**

<img src="https://github.com/manthanpatel98/TFOD_Installation-Object_Detection/blob/main/tfod_images/Screenshot%20(331).png" width="650">

