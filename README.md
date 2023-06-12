# Cell Nuclei Image Segmentation


### 1. Project Description
  * The nuclei inside every cell in our body contains information that can explain about what happpen inside the cell. For exmple the DNA that contains within the nuclei can tell about the diseases such as cancer, heart disease and many more rare disorders. Identification of nuclei in cells can help researchers to find faster solution for every disease that found. Therefore, an automated artificial intelligence model are needed in helping to identify the images of cell nuclei.
  * In this project, a semantic image segmentation model is developed to make prediction of the nuclei. 

  

### 2. Software used, framework,how to run project
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
         

 
 
### 3. Results
1. The architecture model that is used in this project is **_Long Short Term Memory(LSTM)_** ,number of nodes is 64 nodes & window size is 30 LSTM, Dense, and Dropout layers have been implemented in the
model.

![model_architecture](https://github.com/dalila28/covid19-case-prediction/blob/main/images/model_architecture.png)


2. Below are the snapshot of the model performance under 100 epochs which **_Mean Squared Error(MSE)_** as loss & **_Mean Absolute Percentage Error (MAPE)_** as metrics
![model_performance1](https://github.com/dalila28/covid19-case-prediction/blob/main/images/model_performance1.png)
![model_performance2](https://github.com/dalila28/covid19-case-prediction/blob/main/images/model_performance2.png)

3. Tensorboard snapshot showing graph of MSE
![tensorboard](https://github.com/dalila28/covid19-case-prediction/blob/main/images/tensorboard.png)


4. Figure below showing the matplotlib graph comparison between actual & predicted result of covid-19 case in Malaysia based on my deep learning project. From the graph we can see that the predicted line is following the curve of actual line which as for my observation I can say that the result is good eventhough it not following correctly the spike of curve. If we want to improve the result, I think we can increase number of epochs so model has more opportunities to learn from the data and adjust its parameters to improve performance.
![actual_vs_predicted](https://github.com/dalila28/covid19-case-prediction/blob/main/images/actual_vs_predicted.png)


### 4. Credits
1. The data on the COVID-19 epidemic in Malaysia is sourced from the official repository, https://github.com/MoH-Malaysia/covid19-public which is powered by CPRC, CPRC Hospital System, MKAK, and MySejahtera.
2. For creating tensorboard, I refer tutorial from https://www.tensorflow.org/tensorboard/get_started
3. Regarding the tensorflow API that I used in my project, I always refer to this documentation https://www.tensorflow.org/api_docs/python/tf/all_symbols
