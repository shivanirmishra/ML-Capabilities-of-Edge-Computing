## **YOLOV5**

### **On Jetson-nano**

**Steps:**

1. git clone [https://github.com/ultralytics/yolov5.git](https://github.com/ultralytics/yolov5.git)
2. cd yolov5/
3. pip install -U -r requirements.txt
- download video (sample-mp4-file.mp4)
4. python detect.py --source sample-mp4-file.mp4.mp4

For checking output video

**Path:** /home/arani/shivani/yolo/yolov5/runs/detect/exp2

> curl --upload-file sample-mp4-file.mp4 [https://transfer.sh](https://transfer.sh/)
