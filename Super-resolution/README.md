## **Super Resolution**

### **On Jetson-nano**
>https://github.com/dusty-nv/jetson-inference

**Steps to follow:** (https://github.com/dusty-nv/jetson-inference/blob/master/docs/building-repo-2.md#downloading-models)

1. First, make sure git and cmake are installed:

`$ sudo apt-get update
$ sudo apt-get install git cmake`

2. Then clone the `jetson-inference` project:

`$ git clone https://github.com/dusty-nv/jetson-inference
$ cd jetson-inference
$ git submodule update --init`

3. To create bindings for Python 3.6, install these packages before proceeding:

`$ sudo apt-get install libpython3-dev python3-numpy`

4. Configuring with CMake

`$ cd jetson-inference`    # omit if working directory is already jetson-inference/ from above

`$ mkdir build`

`$ cd build`

`$ cmake ../`

5. Compiling the Project

`$ cd jetson-inference/build`          # omit if working directory is already build/ from above

`$ make`

`$ sudo make install`

`$ sudo ldconfig`

6. Run the project

**Path:** /home/arani/shivani/jetson-hello/jetson-inference/build/aarch64/bin

**Command:** `python imagenet.py images/fruit_0.jpg output.jpg`

This will create an output file with inference.

**Make file as a browser link** : `curl --upload-file output.jpg [https://transfer.sh](https://transfer.sh/)`

This will create a link (for this: [https://transfer.sh/JUyWSq/output.jpg](https://transfer.sh/JUyWSq/output.jpg)) which can be seen through browser.
