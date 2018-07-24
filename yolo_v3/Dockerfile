FROM dmaugis/darknet

RUN apt-key update && apt-get update \
    && apt-get install -y wget \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /darknet
RUN wget https://pjreddie.com/media/files/yolov3.weights
CMD ./darknet detect cfg/yolov3.cfg yolov3.weights data/dog.jpg

