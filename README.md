# MobileBERT
Python API for interacting with pre-trained tflite BERT model provided by Tensorflow

The pre-trained model as well as information on performance can be found here: https://www.tensorflow.org/lite/models/bert_qa/overview.

The tflite model file and the associated "vocab.txt" should be within the same folder as the script.

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
