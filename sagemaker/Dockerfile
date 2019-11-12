FROM nvcr.io/nvidia/pytorch:19.09-py3

RUN apt-get update && yes|apt-get upgrade
RUN apt-get install -y wget \
        curl \
        bzip2 \
        nano \
        sudo \
        apt-utils \
        dpkg \
        gnupg2 \
	nginx \
        software-properties-common


ENV PATH="/opt/ml/code:${PATH}"
WORKDIR /opt/ml/code

RUN mkdir /opt/ml/code/yolo
COPY yolo/. /opt/ml/code/yolo/.
RUN cd /opt/ml/code/yolo/darknet && \
	sudo make  && \
	./darknet
