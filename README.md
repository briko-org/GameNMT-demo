# Briko's GameNMT Demo
Briko's GameNMT Demo can be found at: https://www.briko.org/demo

If you'd like to try the pre-trained model at a local environment for a test yourself, here is a simple tutorial you can follow:

#### 1.Download this repository:
```
$ git clone git@github.com:briko-org/GameNMT-demo.git
```
\
It contains the code you need to run the pre-trained ***transformer*** model.
\
For demonstration purpose, we assume that you have download ***GameNMT-demo*** project to your $HOME directory.

#### 2.Install Python (3.6):
```
$ sudo add-apt-repository ppa:jonathonf/python-3.6
$ sudo apt-get update
$ sudo apt-get install python3.6
```
#### 3.Install TensorFlow (TensorFlow 1.12.0)
\
CPU-only:
```
$ pip3 install https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-1.12.0-cp36-cp36m-linux_x86_64.whl
```
GPU-only:
```
$ pip3 install https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.12.0-cp36-cp36m-linux_x86_64.whl
```
#### 4.Add the GameNMT-demo/models folder to the Python path with the command:
```
$ export PYTHONPATH="$PYTHONPATH:$HOME/GameNMT-demo/models"
```
#### 5.Install dependencies:
```
$ pip3 install --user -r $HOME/GameNMT-demo/models/official/requirements.txt
```

#### 6.Export variables
```
PARAM_SET=base
DATA_DIR=$HOME/GameNMT-demo/models/official/transformer/data
MODEL_DIR=$HOME/GameNMT-demo/models/official/transformer/model_$PARAM_SET
VOCAB_FILE=$DATA_DIR/vocab.file
```
#### 7.Download the trained model to MODEL_DIR:
\
[Download Torrent](https://github.com/briko-org/GameNMT-demo/raw/master/models/official/transformer/model_base/Download.torrent)

#### 8.Finally, you can try to translate some text using the trained model with the command below:
```
$ python3.6 $HOME/GameNMT-demo/models/official/transformer/translate.py --model_dir=$MODEL_DIR --vocab_file=$VOCAB_FILE \
    --param_set=$PARAM_SET --text="hello world"
```
