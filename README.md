How to run: python3 main.py -i day3_30.mp4 -o day3_30-custom.avi -y yolo/

(needs weight in yolo folder)


When training:
  OPENCV=0
  CUDNN=0
    PATH=/usr/local/cuda/bin:$PATH make -j$(nproc)
    ./darknet detector train custom_data/detector.data custom_data/cfg/yolov3-custom.cfg darknet53.conv.74 yolov3-custom
