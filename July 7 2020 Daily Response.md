# Daily Response for Tuesday, July 07, 2020 (Day 2)

**1) In Laurence Maroney’s video, What is ML, he compares traditional
programming with machine learning and argues that the main difference
between the two is a reorientation of the rules, data and answers. According
to Maroney, what is the difference between traditional programming and
machine learning?**

Machine learning differes from traditional programming in the following way:

Traditional programming requires the input of rules and data to output some answers. In this case, programers are working to figure out the rules, input that in with the data, to give us some answer.

Machine learning requires some answers and data to output rules. In this case, through a process of labelling, prgrammers get lots of data, which they know the answers to. They use that to establish the rules that will match one to the other.



**2)  With the first basic script that Maroney used to predict a value output from
the model he estimated (he initially started with 10 that predicted ~31.
Modify the predict function to produce the output for the value 7. Do this
twice and provide both answers. Are they the same? Are they different?
Why is this so?**

When I first ran it, I got: *22.002747*. The second time, I got: *21.99807*. These are clearly two different numbers. This occurs because neural networks deal with probabilities. The optimizer (*sgd*) uses the results of the loss function [*mean_squared_error*] (which measures how good or bad the guess that the neural network made is) to create another guess. As this process goes on and on until a result is reached. Since we're dealing in probabilities, and we are using very few data points, the number will change very slightly (as the neural network will predict that there is a very high probability that it will be close to 22).


**3) Using the script you produced to predict housing price, take the provided six
houses and train a neural net model that estimates the relationship between
them. Based on this model, which of the six homes present a good deal?
Which one is the worst deal? Justify your answer.**
Below is my code for the housing prices example. I do not see the information about the 6 houses anywhere. I would input them into xs and ys (and relabel them according to the information given). Since I do not know the nature of the data, I cannot complete this. I will update this answer once I have access to the data.

import tensorflow as tf
import numpy as np
from tensorflow import keras
model=tf.keras.Sequential([keras.layers.Dense(units=1, input_shape=[1])])
model.compile(optimizer='sgd', loss='mean_squared_error')
number_bedrooms=xs
cost_of_house=ys
xs=np.array([1.0, 2.0, 3.0, 4.0, 5.0, 6.0], dtype=float)
ys=np.array([1.0, 1.5, 2.0, 2.5, 3.0, 3.5], dtype=float)
model.fit(xs, ys, epochs=500)
print(model.predict([7.0]),' hundred thousand dollars.')
