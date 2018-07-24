FROM nvidia/cuda:9.2-cudnn7-devel-ubuntu16.04

RUN apt-key update && apt-get update \
    && apt-get install -y git wget patch curl pkg-config  libopencv-dev \
    && rm -rf /var/lib/apt/lists/*

COPY Makefile.patch .
RUN git clone https://github.com/pjreddie/darknet 
WORKDIR /darknet
RUN patch < ../Makefile.patch
RUN make

#RUN wget https://pjreddie.com/media/files/yolov3.weights
#RUN ./darknet detect cfg/yolov3.cfg yolov3.weights data/dog.jpg

