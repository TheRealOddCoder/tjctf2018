# Learn_My_Flag


Learn my flag is not a sort of challenge you usually see in a ctf.

Running file on the downloaded file, gives this
![file_hdf5](https://user-images.githubusercontent.com/42334661/44017454-000be95e-9ef6-11e8-84cb-ef1c070104e0.png)

As soon as I saw that this is a hdf5 file(.h5 file), i knew this task has something to do with machine learning.
If you haven't learnt anything about neural network, figuring out this task will be difficult.

I opened the file using keras library in python
```python
   from keras import models
   model = models.load_model('learn_my_flag','r')
```

Initially i thought it is a image classifier. So, sending an image as input would produce a sample output.
### Note: Since this is a saved model, it is not necessary to run model.compile()


I got a different error as output, saying the expected output size is 1. Then running model.summary() gave me the model layers and size expected.

![model_summary](https://user-images.githubusercontent.com/42334661/44017934-be3af662-9ef7-11e8-8a63-480ddfad1fcf.jpeg)

Knowing the layers it was easy then


