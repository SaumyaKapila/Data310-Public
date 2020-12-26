**What is TF Hub? How did you use it when creating your script for “text classification of movie reviews”?**


TF Hub (or tenser flow hub) is basically a database or storage space for many useful Machine Learning tools, like trained models and datasets. In creating the script for “text classification of movie reviews”, we used this to load trained models in a single line of code. We downloaded the movie review database (IMDB database).



**What are the optimizer and loss functions? How good was your “text classification of movie reviews” model?**


The loss function looks at how good the machine was in guessing the correct classification to the correct review. Then, the optimizer takes that information and uses it to make a new guess. The loss function being used is Binary Crossentropy and the optimizer function being used in this case is adam. This showed a loss of about 0.36 and an accuracy of about 85%, which seems relatively good.


**In “text classification with preprocessed text” you produced a graph of training and validation loss. Add the graph to this response and provide a brief explanation.**

![July 9 Graph 1](https://github.com/SaumyaKapila/Data310-Public/blob/master/Graph%201%20ML%20july%209.png?raw=true)

This graph shows the training and validation loss. As explained previously, the loss function measures how much error (or loss) there was in the model. So, while training for example, as the model trains for more epochs, the model gets more accurate, and therefore, loss should decrease. For this particular graph, I ran it for 20 epochs. At around 8 epochs, the training and validation loss began to diverge. As you can see from the graph above, as the number of epochs increases, the loss decreases, so it does follow the same general pattern of the loss function.

 **Likewise do the same for the training and validation accuracy graph.**
 
 ![July 9 Graph 2](https://github.com/SaumyaKapila/Data310-Public/blob/master/Graph%202%20ML%20July%209.png?raw=true)

For this graph I ran it for 20 epochs. This graph shows that model is overfit, as the training accuracy is greater than the validation accuracy starting at 8 epochs. While the accuracy is increasing overall, at about 8 epochs the accuracy plateaus. Based on this information, we might consider stopping the training of the model at 10 epochs, rather than continuing on to 20 epochs. A better method would be to use EarlyStopping callback which can specify to stop training once the loss has minimized. Regardless, this graph shows training and validation accuracy; as the number of epochs go up, so should the accuracy (since the model should become more accurate), which is the trend that the graph is showing. 

**Sources for today's daily response:**

https://www.tensorflow.org/api_docs/python/tf/keras/callbacks/EarlyStopping?version=nightly

https://www.tensorflow.org/tutorials/keras/text_classification

https://www.tensorflow.org/tutorials/keras/text_classification_with_hub

https://tfhub.dev/


*Note: I struggled with getting the correct graphs for 3 and 4. After trying many variations of code (I wasn't sure if this was supposed to be the exercise or the IMDB data from the example, I ended up using the exercise for the graph. I did so because it seemed to resemble the correct trend more closely (loss decreases, accuracy increases, the training and validation should follow somewhat similar trends, etc.). However, if this is incorrect, please let me know and I will redo it.*
