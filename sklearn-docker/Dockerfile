# Pull base image.
FROM ubuntu:17.10

# Install Python.
RUN \
  apt-get update && \
  apt-get install -y python3 python3-dev python3-pip python3-virtualenv && \
  cd /usr/local/bin && \
  ln -s /usr/bin/python3 python && \
  pip3 install --upgrade pip && \
  rm -rf /var/lib/apt/lists/*

ADD app.py /
ADD ../resources/activity.zip /

# Define working directory.
WORKDIR /

RUN python -m pip install flask
RUN python -m pip install pandas
RUN python -m pip install scipy
RUN python -m pip install sklearn
RUN python -m pip install category_encoders
CMD [ "python", "./app.py"]
