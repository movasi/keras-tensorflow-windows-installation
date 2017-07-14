# Keras-TensorFlow-GPU-Windows-Installation
10 easy steps on the installation of TensorFlow-GPU and Keras in Windows

## 1. Install Anaconda python

### 1.1: Install Anaconda (Python 3.6 version) <a href="https://www.continuum.io/downloads" target="_blank">Download</a>
<p align="center"><img width=70% src="anaconda_windows_installation.png"></p>

### 1.2: Update Anaconda
Open Anaconda Prompt to type the following command(s)
```Command Prompt
conda update conda
conda update --all
```

### 1.3: Install python IDE
Install your favorite python IDE (Python Tools for Visual Studio, PyCharm, Ninja...)


## 2. If you have GPU, install CUDA and cuDNN

### 2.1: Install CUDA Tookit 8.0 <a href="https://developer.nvidia.com/cuda-downloads" target="_blank">Download</a>
Choose your version depending on your Operating System

<p align="center"><img width=70% src="cuda8_windows7_local_installation.png"></p>

For more information, refer to <a href="http://docs.nvidia.com/cuda/cuda-installation-guide-microsoft-windows/index.html">official documentation.</a>

### 2.2: Download cuDNN <a href="https://developer.nvidia.com/rdp/cudnn-download" target="_blank">Download</a>
Choose your version depending on your Operating System.
Membership registration is required.

<p align="center"><img width=70% src="cuDNN_windows_download.png"></p>

Put your unzipped folder in C drive as follows: 
```Command Prompt
C:\cudnn-8.0-windows10-x64-v5.1
```
### 2.3: Add cuDNN into Environment PATH <a href="https://kb.wisc.edu/cae/page.php?id=24500" target="_blank">Tutorial</a>

Add the following path in your Environment.
Subjected to changes in your installation path.
```Command Prompt
C:\cudnn-8.0-windows10-x64-v5.1\cuda\bin
```

Turn off all the prompts. 
Open a new command prompt and type the following command
```Command Prompt
echo %PATH%
```
You shall see that the new Environment PATH is there.

## 3. Install TensorFlow

### 3.1: Create an Anaconda environment with Python=3.5
Open command prompt (**as an administrator**) and type the following command
```Command Prompt
conda create -n tensorflow python=3.5 numpy scipy matplotlib spyder
```

### 3.2: Activate the environment
In the command prompt type the following command
```Command Prompt
activate tensorflow
```

### 3.3.1: If you have a GPU, install TensorFlow-GPU-1.0.1
In the command prompt type the following command
```Command Prompt
pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/windows/gpu/tensorflow_gpu-1.0.1-cp35-cp35m-win_amd64.whl
```

### 3.3.2: If you don't have a GPU, install CPU version of TensorFlow
In the command prompt type the following command
```Command Prompt
pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/windows/cpu/tensorflow-1.2.1-cp35-cp35m-win_amd64.whl
```

For more information, refer to <a href="https://www.tensorflow.org/install/install_windows">official documentation.</a>

## 4. Install Keras
In the command prompt type the following command
```Command Prompt
pip install keras
```

## 5. Test the installation
Let's try running ```examples/mnist_mlp.py``` in your prompt.

Open command prompt in the ```examples``` folder and type the following commands
```Command Prompt
activate tensorflow
python mnist_mlp.py
```
Congratulations ! You have successfully run Keras (with Tensorflow backend) over CPU/GPU on Windows!

<p align="left"><img width=100% src="installation_success.png"></p>
