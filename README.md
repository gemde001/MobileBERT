# MobileBERT
Python API for interacting with pre-trained tflite BERT model provided by Tensorflow

BERT, or Bidirectional Encoder Representations from Transformers, is a method of pre-training language representations which obtains state-of-the-art results on a wide array of Natural Language Processing tasks.

The pre-trained model as well as information on performance can be found here: https://www.tensorflow.org/lite/models/bert_qa/overview.

The tflite model file and the associated "vocab.txt" should be within the same folder as the script.

The model takes a passage and a question as input, then returns a segment of the passage that most likely answers the question. 

This API has been tested with Python 3.6.9 and tensorflow 2.1.0.

Requirements:
```
tensorflow
bert-for-tf2
numpy

```


Running an inference:

```python
  from mobilebert import MobileBERT
  m = MobileBERT()
  answer = m.run(
    "this is a request for information",
    "this is a body of text that contains the answer to the given request"
    )
    print(answer)
```
