# deeplearning-containers

## Choose an image.

Ex: jupyter-cuda11.0-tensorflow2.4.0

## Build the image

```
IMAGE=jupyter-cuda11.0-tensorflow2.4.0
cd dockerfiles/${IMAGE}
sudo docker build -t ${IMAGE} .
```

## Run the image

```
sudo docker run --rm -it -p 8888:8888 --name ${IMAGE}_container ${IMAGE}
```

#### If image uses CUDA, run with `nvidia-docker` instead:


```
sudo nvidia-docker run --rm -it -p 8888:8888 --name ${IMAGE}_container ${IMAGE}
```
