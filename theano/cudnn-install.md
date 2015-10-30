# CuDNN from NVIDIA: install on Ubuntu

To install CuDNN, download and extract archive from NVIDIA's website.

Then copy the files from the extracted folders to the installation path of cuda in `/usr/local/cuda-7-0/` using the following commands:

```
sudo cp include/cudnn.h /usr/local/cuda-7.0/include
sudo cp lib64/libcudnn* /usr/local/cuda-7.0/lib64
```

