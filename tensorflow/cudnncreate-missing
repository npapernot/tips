# cudnnCreate missing 

This error `could not find cudnnCreate in cudnn DSO` simply indicates that the cuDNN package is missing. To fix it, download archive from [NVIDIA](https://developer.nvidia.com/cudnn) and run:

```
tar xvzf cudnn-7.5-linux-x64-v4.tgz
sudo cp cuda/include/cudnn.h /usr/local/cuda/include
sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64
sudo chmod a+r /usr/local/cuda/include/cudnn.h /usr/local/cuda/lib64/libcudnn*
```
