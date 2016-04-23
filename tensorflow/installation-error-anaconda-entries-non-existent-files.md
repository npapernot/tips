# Installation Error caused by Anaconda when using `pip` to install TensorFlow

When seeing this error during a TensorFlow install using a non-sudo pip
install: 

``` Cannot remove entries from nonexistent file /home/<username>/anaconda/lib/python2.7/site-packages/easy-install.pth 
```

simply download the package directly from the URL indicated in the
documentation. At time of writing, it is:

```
https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.8.0rc0-cp27-none-linux_x86_64.whl
```

and run `pip install tensorflow-0.8.0rc0-cp27-none-linux_x86_64.whl` from
directory with downloaded package.

