# Install-tensorflow-gpu
Introduction to install tensorflow-gpu

(1) Install CUDA (download here:https://developer.nvidia.com/cuda-downloads)
please choose installer type : deb(local)

`sudo dpkg -i cuda-repo-ubuntu1604-8-0-local-ga2_8.0.61-1_amd64.deb` 

`sudo apt install -f`

`sudo apt-get update`

`sudo apt-get install cuda`

(2) Install CuDNN (download here: https://developer.nvidia.com/developer-program/signup)

First, you need to sign up an account, after activated your account please go to Compute Works> Deep learning> Software > cuDNN Download  
Download these two files based on your OS: cuDNN v7.0 Runtime Library for Ubuntu16.04 (Deb), cuDNN v7.0 Developer Library for Ubuntu16.04 (Deb) 


`sudo dpkg -i libcudnn7_7.0.1.13-1+cuda9.0_amd64.deb`

`sudo dpkg -i libcudnn7-dev_7.0.1.13-1+cuda9.0_amd64.deb`

(3) Edit bashrc file

`sudo vi ~/.bashrc`

Add following three lines to the file

`export LD_LIBRARY_PATH="$LD_LIBRARY_PATH:/usr/local/cuda/lib64:/usr/local/cuda/extras/CUPTI/lib64"`

`export CUDA_HOME=/usr/local/cuda`

`export PATH=$PATH:/usr/local/cuda/bin`

Save and exit file

`source ~/.bashrc`

(4) Install tensorflow-gpu

Python2: `pip install --upgrade tensorflow-gpu`

Python3: `pip3 install --upgrade tensorflow-gpu`

(5) Testing

python

import tensorflow as tf
