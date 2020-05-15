# LaneTracker
Using Keras to build a deep learning model for lane lines tracking
* This model use the basic encoder-decoder and LSTM architecture to track lines frame-by-frame.

## Installation
```
pip install -r requirements.txt
```

## Data
* The training data comes from [CULane](https://xingangpan.github.io/projects/CULane.html).
* Using [culane2tusimple](https://github.com/BurkeyLai/culane2tusimple) to transform data format to TuSimple's format.

## Training
* 17622 sequence frames for training, 8811 for validation and 2938 for testing.
* Currently, the model is trained to track the right line of driving lane.
* Training for 250 epochs and batch size set to 64.
* Below is the architecture:

![Network](/image/en_lstm_de_model_bs64.png)
* Training loss:
![Network](/image/下載.png)

## Test model
* The model need the previous 5 frames as input, and it can track the lines in the 6th frame as output.

`6 ground truth frames`
![Network](/image/下載3.png)

`Tracking result in 6th frames`
![Network](/image/下載4.png)
