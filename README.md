# docker-images


#### ikigeg/node-8-alpine-journey
This image contains node_modules that require compiling, these are specific to the image-webpack-loader module.

For image-webpack-loader@3.6.0:
```
docker build --squash -t ikigeg/node-8-alpine-journey:3.6.0 node-alpine-iwl-3.6.0
docker push ikigeg/node-8-alpine-journey:3.6.0
```

For image-webpack-loader@4.6.0:
```
docker build --squash -t ikigeg/node-8-alpine-journey:4.6.0 node-alpine-iwl-4.6.0
docker push ikigeg/node-8-alpine-journey:4.6.0
```