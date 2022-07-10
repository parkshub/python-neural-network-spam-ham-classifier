## Neural Network: Spam Filter

![img]('alina-grubnyak-ZiQkhI7417A-unsplash.jpg')

### Background
For this project, I challenged myself to build and train a neural network to successfully detect spam, text messages. I've manually coded the functions for gradient checking, and forward and back propogation by using matrix multiplication. The training dataset was derived from https://www.kaggle.com/rushirdx/spam-and-ham-dataset. Throughout the project, I explore various topics such as bias vs. variance trade-off, regularization, optimization, hyper-parameter tuning and batch gradient descent. Then, I compare the models' accuracy and speed using matplotlib. After determining the best model, I ran a test on my own text messages, which turned about to a great success!

### Discussion
I started this project to apply what I've learned from professor Andrew Ng's Coursera lectures and other online courses. I purposely avoided using APIs to better demonstrate my knowledge of neural networks. What I had anticipated taking, at most, 2 weeks turned into 2 and a half months. Initially, I had outlined an even larger project where I would tune the hyperparameters and compare other regularization and optimization techniques—exponential learning rate decay, batch normalization, principal component analysis (PCA), and drop-out regularization. However, I quickly realized the barriers to taking on such a large project, with the main one being time. I had tested a short script to tune the learning rate and the estimated time came out to be over a week. Thankfully, due to Adam optimization’s genius, I was able to avoid tuning hyperparameters.

If you have taken a look at “module.ipynb” and “model.ipynb,” you may have noticed that the cost function isn't embedded in the model. Originally, the cost function was called after the forward propagation function. It received the outputs from forward prop and calculated the cost, but due to an issue—which I believe was due to a rounding error caused by Numpy—gradient checking indicated something was wrong. I tested the model with a simpler 2 x 2 dataset and compared the outputs with my manual calculations, and weirdly, everything seemed to be in order. While searching for the cause, I had discovered a couple minor mistakes. My dictionary-to-vector function was flattening the parameters in the wrong order, but, to my surprise, it had no bearing on the results. Regardless, it was fixed. After two weeks of unnecessarily tinkering with my forward prop, backprop, and cost function, I found the issue and embedded the cost function inside forward propagation instead of the model. I’ve left some of the previous versions of the functions in the module for the reader’s viewing, but ulteriorly because I’m afraid to erase them.

With all the frustrations aside, I genuinely enjoyed working on this project. Through this experience, I've gained an abundance of valuable hands-on experience, not just about neural networks, but coding in general. If you have any questions about the project, or would like to provide feedback, please email me at AndrewJHPark@protonmail.com.


**please begin with "neural_network.ipynb" and refer to the files in folders "modules" and "saved_data" for clarity. This project was completed using Gradient Notebooks and their PyTorch repository (Python version 3.8.12). A list of the necessary packages can be found in "requirements.txt."**

**As of March 28th, 2022, "neural_network.ipynb" is missing some outputs. Please refer to "neural_network.pdf" or download and load "neural_network.html."**
