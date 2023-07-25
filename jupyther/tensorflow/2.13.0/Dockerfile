FROM tensorflow/tensorflow:2.13.0-gpu-jupyter
RUN /usr/bin/python3 -m pip install --upgrade pip

RUN pip install pandas \
  sklearn \
  scipy \
  matplotlib \
  imutils \
  opencv-python

RUN apt-get update
RUN apt-get install -y git \
  wget \
  libgl1-mesa-glx

ENV NB_PREFIX /

CMD ["sh","-c", "jupyter notebook --notebook-dir=/home/jovyan --ip=0.0.0.0 --no-browser --allow-root --port=8888 --NotebookApp.token='' --NotebookApp.password='' --NotebookApp.allow_origin='*' --NotebookApp.base_url=${NB_PREFIX}"]
