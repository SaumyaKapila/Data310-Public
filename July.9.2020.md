**What is TF Hub? How did you use it when creating your script for “text classification of movie reviews”?**


TF Hub (or tenser flow hub) is basically a database or storage space for many useful Machine Learning tools, like trained models and datasets. In creating the script for “text classification of movie reviews”, we used this to load trained models in a single line of code. We downloaded the movie review database (IMDB database).



**What are the optimizer and loss functions? How good was your “text classification of movie reviews” model?**


The loss function looks at how good the machine was in guessing the correct label to the correct review. Then, the optimizer takes that information and uses it to make a new guess. The loss function being used is Binary Crossentropy and the optimizer function being used in this case is adam. This showed a loss of about 0.36 and an accuracy of about 85%, which seems relatively good.


**In “text classification with preprocessed text” you produced a graph of training and validation loss. Add the graph to this response and provide a brief explanation.**

![July 9 Graph 1](https://github.com/SaumyaKapila/Data310-Public/blob/master/Graph%201%20ML%20july%209.png?raw=true)

This graph shows the training and validation loss. As explained previously, the loss function measures how much error (or loss) there was in the model. So, while training for example, as the model trains for more epochs, the model gets more accurate, and therefore, loss should decrease. For this particular graph, I ran it for 20 epochs. At around 8 epochs, the training and validation loss began to diverge. As you can see from the graph above, as the number of epochs increases, the loss decreases, so it does follow the same general pattern of the loss function.

 **Likewise do the same for the training and validation accuracy graph.**
 
 ![July 9 Graph 2](https://github.com/SaumyaKapila/Data310-Public/blob/master/Graph%202%20ML%20July%209.png?raw=true)

For this graph I ran it for 20 epochs. This graph shows that model is overfit, as the training accuracy is greater than the validation accuracy starting at 8 epochs. While the accuracy is increasing overall, at about 8 epochs the accuracy plateaus. Based on this information, we might consider stopping the training of the model at 10 epochs, rather than continuing on to 20 epochs. Regardless, this graph shows training and validation accuracy; as the number of epochs go up, so should the accuracy (since the model should become more accurate), which is the trend that the graph is showing. 
