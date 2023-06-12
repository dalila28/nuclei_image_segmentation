# Cell Nuclei Image Segmentation


## 1. Project Description
  * The nuclei inside every cell in our body contains information that can explain about what happpen inside the cell. For example DNA that contains within the nuclei can tell about the diseases such as cancer, heart disease and many more rare disorders. Identification of nuclei in cells can help researchers to find faster solution for every disease that found. Therefore, an automated artificial intelligence model are needed to identify the images of cell nuclei.
  * In this project, a semantic image segmentation model is developed to make prediction of the nuclei. 

  

## 2. Software used, framework,how to run project
   * Software needed:
     * Visual Studio Code as my IDE. You can get here https://code.visualstudio.com/download
     * Anaconda. https://www.anaconda.com/download

   * Framework:
     * I use Tensorflow and Keras framework to develop this deep learning project, as for Keras it already a part of TensorFlow’s core API.
   
   * How to run project:
     * Download project in the github
     * In Visual Studio Code make sure install Python
     * Open Anaconda prompt : "(OPTIONAL) IS FOR GPU INSTALLATION IF YOU NEED FOR CPU THEN IGNORE OPTIONAL"
        * (base) conda create -n "name u want to have" python=3.8
        * (env) conda install -c anaconda ipykernel
        * conda install numpy,conda install pandas,conda install matplotlib (run each of this one by one)
        * (OPTIONAL) conda install -c anaconda cudatoolkit=11.3
        * (OPTIONAL) conda install -c anaconda cudnn=8.2
        * (OPTIONAL) conda install -c nvidia cuda-nvcc
        * conda install git
        * 1 (a) create a folder named TensorFlow inside the tensorflow environment. For example: “C:\Users\< USERNAME >\Anaconda3\envs\tensorflow\TensorFlow”
        * (b) type: cd “C:\Users\<USERNAME>\Anaconda3\envs\tensorflow\TensorFlow” (to change directory to the newly created TensorFlow folder) 
        * (c) type: git clone https://github.com/tensorflow/models.git
        * conda install -c anaconda protobuf
        * 2 (a) type: cd “C:\Users\< USERNAME >\Anaconda3\envs\tensorflow\TensorFlow\models\research” (into TensorFlow\models\research for example)
        * b) type: protoc object_detection/protos/*.proto --python_out=.
        * 3 a) pip install pycocotools-windows
        * b) cp object_detection/packages/tf2/setup.py .
        * c) python -m pip install .
      * Test your installation (RESTART TERMINAL BEFORE TESTING)  
         * Inside C:\Users\< USERNAME > \Anaconda3\envs\tensorflow\TensorFlow\models\research
         * python object_detection/builders/model_builder_tf2_test.py The terminal should show OK if it passes all the tests
       * Open Visual Studio Code, 
         * Go to open new folder, open downloaded file that you download from my repository
         * Make sure downloaded dataset and the concrete_crack.py file in same folder
         * ![ #A020F0](https://placehold.co/15x15/A020F0/A020F0.png) **ATTENTION!!! : root_path = "Please change the path according to your folder path" DON'T FOLLOW MY PATH IN THE concrete_crack.py FILE SINCE THE PATH IS MY OWN FOLDER PATH**       
         * Then you can run concrete_crack.py file
         * **Troubleshoot: let say you have problem loading the dataset, please check your folder path carefully**
         

 
 
## 3. Results
### Model Architecture
For the model architecture, U-NET model architecture has been built for this project 

![model_architecture](https://github.com/dalila28/nuclei_image_segmentation/blob/main/images/architecture.png)

                                                           Model Architecture


### 2. Model performance



   * Snapshot of model performance below showing that the model should undergo 100 epochs of training, but with the implementation of early stopping during training, the model just undergo 17 epochs of training. It is because  EarlyStopping callback can detect if the model's performance is not improving on new data, which is as an indication that the model is no longer learning meaningful patterns and further training may not be beneficial. Therefore, training will stop early to avoid overfitting. During my model training, both training and validation achieved 96%of accuracy and I can say that my model perform optimally as the difference of values between training loss and validation loss is just small gap.
   

![model_performance](https://github.com/dalila28/nuclei_image_segmentation/blob/main/images/model_performance.png)

                                                       Model Performance


  *   In short, application of early stopping callbacks in the model training can avoid our model to be overfitted.
  


### 3. Data inspection


![data inspection](https://github.com/dalila28/nuclei_image_segmentation/blob/main/images/data_inspection.png)


### 4. Output Prediction

![predict1](https://github.com/dalila28/nuclei_image_segmentation/blob/main/images/predict1.png)



![predict2](https://github.com/dalila28/nuclei_image_segmentation/blob/main/images/predict2.png)



![predict3](https://github.com/dalila28/nuclei_image_segmentation/blob/main/images/predict3.png)




![predict4](https://github.com/dalila28/nuclei_image_segmentation/blob/main/images/predict4.png)


                                                      


## 5. Credits
1. Title: Data Science Bowl 2018 - Kaggle Competitions
   Website: Kaggle
   URL: https://www.kaggle.com/competitions/data-science-bowl-2018/overview
2. I followed the TensorBoard tutorial provided by TensorFlow, available at https://www.tensorflow.org/tensorboard/get_started, to create visualizations for monitoring and analyzing models.
3. To ensure efficiency in my project, I consistently relied on the comprehensive TensorFlow API documentation at https://www.tensorflow.org/api_docs/python/tf/all_symbols. This documentation served as my go-to resource for exploring the various functions, classes, and modules provided by TensorFlow, enabling me to effectively utilize the powerful TensorFlow framework in my project.
