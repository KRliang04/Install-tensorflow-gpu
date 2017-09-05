# Install-tensorflow-gpu
Introduction to install tensorflow-gpu

(1) Install CUDA (download here:https://developer.nvidia.com/cuda-downloads)
please choose installer type : deb(local)

`sudo dpkg -i cuda-repo-ubuntu1604-8-0-local-ga2_8.0.61-1_amd64.deb` 

`sudo apt install -f`

`sudo apt-get update`

`sudo apt-get install cuda`

(2) Install CuDNN (download here: https://developer.nvidia.com/developer-program/signup)

First, you need to sign up an account, after activated your account please download these two files based on your OS: cuDNN v5.1 Runtime Library for Ubuntu14.04 (Deb), 
cuDNN v5.1 Developer Library for Ubuntu14.04 (Deb) 
#### In this case Ubuntu 14.04 is also applicable to Ubuntu 16.04

`sudo dpkg -i libcudnn5_5.1.5-1+cuda8.0_amd64.deb`

`sudo dpkg -i libcudnn5-dev_5.1.5-1+cuda8.0_amd64.deb`

(3) Edit bashrc file

`sudo vi ~/.bashrc`

add following two lines to the file

`export LD_LIBRARY_PATH="$LD_LIBRARY_PATH:/usr/local/cuda/lib64:/usr/local/cuda/extras/CUPTI/lib64"`

`export CUDA_HOME=/usr/local/cuda`

`source ~/.bashrc`

(4) Install tensorflow-gpu

Python2: `pip install tensorflow-gpu`
Python3: `pip3 install tensorflow-gpu`

(5) Testing

python

import TensorFlow as tf
