**What is TF Hub? How did you use it when creating your script for “text classification of movie reviews”?**


TF Hub (or tenser flow hub) is basically a database or storage space for many useful Machine Learning tools, like trained models and datasets. In creating the script for “text classification of movie reviews”, we used this to load trained models in a single line of code. We downloaded the movie review database (IMDB database).



**What are the optimizer and loss functions? How good was your “text classification of movie reviews” model?**


The loss function looks at how good the machine was in guessing the correct label to the correct image. Then, the optimizer takes that information and uses it to make a new guess. The loss function being used is Binary Crossentropy and the optimizer function being used in this case is adam. This showed a loss of about 0.36 and an accuracy of about 85%, which seems relatively good.


**In “text classification with preprocessed text” you produced a graph of training and validation loss. Add the graph to this response and provide a brief explanation.**

![July 9 Graph 1](https://github.com/SaumyaKapila/Data310-Public/blob/master/Graph%201%20ML%20july%209.png?raw=true)


 **Likewise do the same for the training and validation accuracy graph.**
