# Real-Time-Face-Detector
Create your own Real-Time World Wide Face Detector using a webcam!! We use powerful python script by [Apokky-30](https://github.com/Apokky-30) to make all of this incredible project.

# Example:
![36f0e3f0-13cb-11e7-8258-4d0c9ce1e419](https://user-images.githubusercontent.com/92684818/138464953-4dd5d06f-a3bc-4102-9ca6-cb18a7a57e2f.gif)

# Installations↙️
## Requirements:
- Python 3.3+ or Python 2.7
- macOS or Linux (Windows not officially supported, but might work)
## Installation Options:
### Installing on Mac or Linux :
#### - First, make sure you have dlib already installed with Python bindings:
[```How to install dlib from source on macOS or Ubuntu```](https://gist.github.com/ageitgey/629d75c1baac34dfa5ca2a1928a7aeaf)
#### - Then, make sure you have cmake installed:
```brew install cmake```
#### - Finally, install this module from pypi using ```pip3``` (or ```pip2``` for Python 2):
```pip3 install face_recognition```
#### Alternatively, you can try this library with [Docker](https://www.docker.com/)
#### If you are having trouble with installation, you can also try out a [pre-configured VM.](https://medium.com/@ageitgey/try-deep-learning-in-python-now-with-a-fully-pre-configured-vm-1d97d4c3e9b)
### Installing on Windows :
While Windows isn't officially supported, helpful users have posted instructions on how to install this library:
- [@masoudr's Windows 10 installation guide (dlib + face_recognition)](https://github.com/ageitgey/face_recognition/issues/175#issue-257710508)
### Installing a pre-configured Virtual Machine image :
- [Download the pre-configured VM image](https://medium.com/@ageitgey/try-deep-learning-in-python-now-with-a-fully-pre-configured-vm-1d97d4c3e9b) (for VMware Player or VirtualBox).
### Installing on an Nvidia Jetson Nano board :
- [Jetson Nano installation instructions](https://medium.com/@ageitgey/build-a-hardware-based-face-recognition-system-for-150-with-the-nvidia-jetson-nano-and-python-a25cb8c891fd)
-- Please follow the instructions in the article carefully. There is current a bug in the CUDA libraries on the Jetson Nano that will cause this library to fail silently if you don't follow the instructions in the article to comment out a line in dlib and recompile it.
### Installing on Raspberry Pi 2+ :
- [Raspberry Pi 2+ installation instructions](https://gist.github.com/ageitgey/1ac8dbe8572f3f533df6269dab35df65)
### Installing on FreeBSD :
```pkg install graphics/py-face_recognition```
### Python Module :
#### You can import the ```face_recognition module``` and then easily manipulate faces with just a couple of lines of code. It's super easy!
#### API Docs: https://face-recognition.readthedocs.io.
# Source Code↙️
#### [View and Download the code from here](https://github.com/Apokky-30/Real-Time-Face-Detector/blob/main/RealTime_face_detector.py) -- by Apokky-30
# Creating a Standalone Executable :
#### If you want to create a standalone executable that can run without the need to install ```python``` or ```face_recognition```, you can use [PyInstaller](https://github.com/pyinstaller/pyinstaller). However, it requires some custom configuration to work with this library. See [this issue](https://github.com/ageitgey/face_recognition/issues/357) for how to do it.
# Articles and Guides that ```cover face_recognition``` :
- My article on how Face Recognition works: [Modern Face Recognition with Deep Learning](https://medium.com/@ageitgey/machine-learning-is-fun-part-4-modern-face-recognition-with-deep-learning-c3cffc121d78)
-- Covers the algorithms and how they generally work
- [Face recognition with OpenCV, Python, and deep learning](https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/) by Adrian Rosebrock
-- Covers how to use face recognition in practice
- [Raspberry Pi Face Recognition](https://www.pyimagesearch.com/2018/06/25/raspberry-pi-face-recognition/) by Adrian Rosebrock
-- Covers how to use this on a Raspberry Pi
- [Face clustering with Python]() by Adrian Rosebrock
-- Covers how to automatically cluster photos based on who appears in each photo using unsupervised learning
# Caveats :
- The face recognition model is trained on adults and does not work very well on children. It tends to mix up children quite easy using the default comparison threshold of 0.6.
- Accuracy may vary between ethnic groups. Please see [this wiki page](https://github.com/ageitgey/face_recognition/wiki/Face-Recognition-Accuracy-Problems#question-face-recognition-works-well-with-european-individuals-but-overall-accuracy-is-lower-with-asian-individuals) for more details.
# Deployment to Cloud Hosts (Heroku, AWS, etc) :
#### Since ```face_recognition``` depends on ```dlib``` which is written in C++, it can be tricky to deploy an app using it to a cloud hosting provider like Heroku or AWS.
#### To make things easier, there's an example Dockerfile in this repo that shows how to run an app built with ```face_recognition``` in a [Docker](https://www.docker.com/) container. With that, you should be able to deploy to any service that supports Docker images.
#### You can try the Docker image locally by running: ```docker-compose up --build```
#### There are also [several prebuilt Docker images.](https://github.com/ageitgey/face_recognition/blob/master/docker/README.md)
#### Linux users with a GPU (drivers >= 384.81) and [Nvidia-Docker](https://github.com/NVIDIA/nvidia-docker) installed can run the example on the GPU: Open the [docker-compose.yml](https://github.com/ageitgey/face_recognition/blob/master/docker-compose.yml) file and uncomment the ```dockerfile: Dockerfile.gpu``` and ```runtime: nvidia``` lines.
# Having problems? :
#### If you run into problems, please read the [Common Errors](https://github.com/ageitgey/face_recognition/wiki/Common-Errors) section of the wiki before filing a github issue.
# Find Me On :
#### [Instagram](https://instagram.com/apokky_)
