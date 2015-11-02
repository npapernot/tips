# Install instructions Ubuntu

Instructions: <http://markus.com/install-theano-on-aws/>


```
sudo apt-get update
sudo apt-get install python-pip python-dev build-essential
sudo pip install --upgrade pip 
sudo pip install --upgrade virtualenv
sudo pip install numpy
sudo apt-get install gfortran libopenblas-dev liblapack-dev
sudo pip install --upgrade https://github.com/Theano/Theano/archive/master.zip
sudo pip install --upgrade https://github.com/Lasagne/Lasagne/archive/master.zip
wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1404/x86_64/cuda-repo-ubuntu1404_7.5-18_amd64.deb
sudo dpkg -i cuda-repo-ubuntu1404_7.5-18_amd64.deb
sudo apt-get update
sudo apt-get install cuda
```


