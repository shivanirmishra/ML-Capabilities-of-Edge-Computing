 ## **360 Video or AR/VR User Eye, Position and Head Movement**
>https://github.com/mtliba/ATSal

### **Datasets**

**1. VR-EYETRACKING DATASETS:**
1. stimuli - https://drive.google.com/file/d/1LhIuvn9MCrE5-UvWvGWnLeR3sco1uG5s/view?usp=sharing 

2. VR - https://drive.google.com/file/d/1Tgtjgrdja-ICDF3KBqN8tI3stFY2g1O-/view?usp=sharing

- For downloading big file do the following steps:

`pip install gdown`

`pip install gshell`

- Syntax to download big file: `gdown https://drive.google.com/uc?id=1Tgtjgrdja-ICDF3KBqN8tI3stFY2g1O-`

**nohup for running process in background**

To unzip both dataset: 
1. nohup unzip stimuli.zip -d stimuli & (output bydefault in nohup.out file)
2. nohup unzip VR.zip -d VR > VR.out & (to save output in VR.out file)

**2. Salient360! and Sitzman Image DATASETS:**

- Done by Sir!!!

**Models Parameters (download using gdown)**

ATSal attention model initialization :
>https://drive.google.com/file/d/1qT4tALLSGmsRfqf_dJ-1nhS_3iT4fFMg/view

ATSal attention model trained on Salient360! and Sitzman image dataset:
>https://drive.google.com/file/d/1dGnufIVaqmKxKm1jvMn65fWa-E4sxld9/view

ATSal attention model trained on Salient360! and VR-EyeTracking video dataset:
>https://drive.google.com/file/d/18tqbKvKgm7jsWUul0F0QsGhKYTg9XOrA/view

ATSal expert models trained on Salient360! and VR-EyeTracking video dataset:
>https://drive.google.com/file/d/1N0u-jZEU6042F2YJDaTvXyCLcv5m-3Tj/view
>https://drive.google.com/file/d/1l1DuvpTeqkS5wJhdHPEdGwxBmi4EFaAc/view

### **Working**

**Dataset used**

- Salient360! and Sitzman Image DATASETS:

**Path:** /shivani/xr/dataset2/Sitzmann/Sitzmann_TVCG_VR/

**Environment:** conda activate xr
(delete pyc file first if exits(already completed))

**Command to run:** python3 test.py /home/ravi/shivani/xr/dataset2/Sitzmann/Sitzmann_TVCG_VR output

**Output:** /shivani/xr/ATSal/test/output

