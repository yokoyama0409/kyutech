FROM python:3.6

RUN mkdir /code
WORKDIR /code

COPY requirements.txt /code/

# opencv-devのインストール
RUN apt-get update -y && apt-get install -y libopencv-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# TensorflowとOpencvのインストール
RUN pip install --upgrade pip
RUN pip install -r requirements.txt
