# tensorflow_OSX_build
TensorFlow whl custom build for OSX with SSE3 4.1 4.2 AVX AVX2 FMA support

TensorFlow

- [x] 1.2.0

- 1. [x] python2.7

- [x] 1.2.1

- 1. [x] python2.7

- [x] 1.3.0

- 1. [x] python2.7

- [x] 1.4.0

- 1. [x] python2.7

compile instructions:
```bash

bazel build -c opt --copt=-mavx --copt=-mavx2 --copt=-msse4.2 --copt=-msse4.1 --copt=-msse3 --copt=-mfma -k //tensorflow/tools/pip_package:build_pip_package

bazel-bin/tensorflow/tools/pip_package/build_pip_package /tmp/tensorflow_pkg

```
installation instruction:
```bash

pip install “your whl path” --upgrade

```
