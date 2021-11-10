 ## **Real-time voice commands/translation**
 >https://github.com/CorentinJ/Real-Time-Voice-Cloning

### **On Server**

#### **Steps**

1. git clone https://github.com/CorentinJ/Real-Time-Voice-Cloning.git

2. Make env with python 3.7

- conda create -n voice python=3.7

3. conda activate voice

4. pip install torch

5. pip install ffmpeg

6. pip install -r requirements.txt

7. **Download Pretrained Models**

- cd Real-Time-Voice-Cloning
> wget [https://github.com/blue-fish/Real-Time-Voice-Cloning/releases/download/v1.0/pretrained.zip](https://github.com/blue-fish/Real-Time-Voice-Cloning/releases/download/v1.0/pretrained.zip)
- unzip pretrained.zip

8. python demo_cli.py --no_mp3_support

**Path:** /home/ravi/shivani/voice_clone/Real-Time-Voice-Cloning/samples/test.wav (must have format other than mp3)

**Sentence:** Anything around 20 to 25 words

Example: This is a GUI-less example of interface to SV2TTS. The purpose of this script is to show how you can interface this project easily with your own. See the source code for an explanation of what is happening.
- It will make an output file in the same repository.

### **On Jetson-nano**

**Installation of aachiconda:** 
> https://github.com/Archiconda/build-tools/releases

#### **Steps**

1. git clone https://github.com/CorentinJ/Real-Time-Voice-Cloning.git

2. Make env with python 3.7

- conda create -n voice python=3.7

3. conda activate voice

4. pip install torch

**Steps to install pytorch (manually):**

- git clone --recursive --branch 1.7 http://github.com/pytorch/pytorch
- cd pytorch
- python3.8 -m pip install -r requirements.txt
- python3.8 setup.py install

5. pip install ffmpeg

6. pip install -r requirements.txt

7. **Download Pretrained Models**

- cd Real-Time-Voice-Cloning
> wget [https://github.com/blue-fish/Real-Time-Voice-Cloning/releases/download/v1.0/pretrained.zip](https://github.com/blue-fish/Real-Time-Voice-Cloning/releases/download/v1.0/pretrained.zip)
- unzip pretrained.zip

8. python demo_cli.py

**Path:** /home/ravi/shivani/voice_clone/Real-Time-Voice-Cloning/samples/test.mp3  (check file name in samples folder and write accordingly)

**Sentence:** Anything around 20 to 25 words

Example: This is a GUI-less example of interface to SV2TTS. The purpose of this script is to show how you can interface this project easily with your own. See the source code for an explanation of what is happening.
- It will make an output file in the same repository.
