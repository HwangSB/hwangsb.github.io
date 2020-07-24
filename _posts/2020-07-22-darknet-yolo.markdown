---
layout: post
title:  "Darknet - YOLOv4"
date:   2020-07-22 17:00:00 +0900
categories: jekyll update
---

# 설치
1. CMake 3.18.0  
2. OpenCV 4.4.0  
3. CUDA 11.0  
4. cuDNN 8.0

# 빌드 전 프로젝트 설정
darknet-master/build/darknet/darknet.sln 실행 > Configuration: Release/x64로 변경  
추가 포함 디렉터리 opencv include  
추가 라이브러리 디렉터리 opencv lib  
darknet-master/build/darknet/darknet.vcxproj 메모장으로 열어 "CUDA 10.0"을 "CUDA 11.0"으로 수정  
환경변수 > 시스템변수 > CUDNN: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.0 추가  
CUDA C/C++ > Device > Code Generation: https://developer.nvidia.com/cuda-gpus#collapse4 (ex GTX 1080TI = compute_61,sm_61)

# YOLOv4
https://github.com/AlexeyAB/darknet

# YOLO mark (라벨링)
https://github.com/AlexeyAB/Yolo_mark

# cfg 파일 생성
darknet-master/cfg/yolov4-custom.cfg 복사 > darknet-master/build/darknet/x64/yolo-obj.cfg로 붙여넣기

## cfg 파일 커스터마이징
[yolo] classes=라벨링한 오브젝트 개수  
[yolo] 바로 위에 있는 [convolutional]에 filter=(classes + 5) * 3  
모든 [yolo] 레이아웃에 대해 동작 수행

# 학습
darknet.exe detector train [data file] [cfg file] [pre-trained weights]

# 예측
darknet.exe detector test [data file] [cfg file] [weights file] [image file]  
darknet.exe detector demo [data file] [cfg file] [weights file] [video file]  
darknet.exe detector demo [data file] [cfg file] [weights file] [webcam]

## 예측 결과 저장
-out_filename [filename]

## 임계값 설정
-thresh [0.0-1.0]

# Video Stopped 에러 발생시
opencv_videoioffmpeg440_64.dll을 darknet.exe와 같은 폴더 안에 넣기

# 참고
https://medium.com/@jonathan_hui/yolov4-c9901eaa8e61  
https://pgmrlsh.tistory.com/6
