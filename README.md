# convox/python

Convox base image for Python

## Usage

    FROM convox/python

    # copy only the files needed for pip install
    COPY requirements.txt /app/requirements.txt
    RUN pip3 install --upgrade pip
    RUN pip3 install -r requirements.txt

    # copy the rest of the app
    COPY . /app

## Expectations

Application using this image should:

* Copy their source files into `/app`

## Exports

None

## Includes

### Base Image: [ubuntu:16.04](https://hub.docker.com/_/ubuntu/)

### Development headers

* `build-essential`
* `python3-dev`

### Python Environment

* `python3-pip`
