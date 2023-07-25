FROM jupyter/tensorflow-notebook:tensorflow-2.13.0

RUN apt-get update
RUN apt-get install -y git \
  wget \
  libgl1-mesa-glx

# install pip
RUN apt-get install -y python3-pip

RUN /usr/bin/python3 -m pip install --upgrade pip

RUN pip install pandas \
  sklearn \
  scipy \
  matplotlib \
  imutils \
  opencv-python



ENV NB_PREFIX /

CMD ["sh","-c", "jupyter notebook --notebook-dir=/home/jovyan --ip=0.0.0.0 --no-browser --allow-root --port=8888 --NotebookApp.token='' --NotebookApp.password='' --NotebookApp.allow_origin='*' --NotebookApp.base_url=${NB_PREFIX}"]
