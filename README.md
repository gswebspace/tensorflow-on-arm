# Tensorflow-on-arm For ODROID C2

Inspired by the [tensorflow-on-arm](https://github.com/lhelontra/tensorflow-on-arm).
Instructions to compile tensorflow specifically for Amlogic ARM® Cortex®-A53(ARMv8) used by ODROID C2.

# Cross-compilation
## Using docker
```shell
cd build_tensorflow/
docker build -t tf-arm -f Dockerfile .
docker run -it -v /tmp/tensorflow_pkg/:/tmp/tensorflow_pkg/ --env TF_PYTHON_VERSION=3.7 tf-arm ./build_tensorflow.sh configs/odroidc2.conf
```
The output .whl file will be available at `/tmp/tensorflow_pkg`

## Edit tweaks like bazel resources, board model, and others
see configuration file examples in: build_tensorflow/configs/
