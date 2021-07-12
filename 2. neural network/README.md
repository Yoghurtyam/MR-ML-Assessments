# Build a neural network from scratch and use it for sentiment analysis

***Problem Brief:*** Build a simple feed forward neural network from the ground-up only using a few external libraries (given below). Then use it to predict what the rating (loosely referred to as sentiment) is for a given phone review (check dataset section). 


You may have previously used neural networks from **Pytorch** or **Tensorflow** in your projects, in this task you will be required to build a neural network from scratch using python. We're not evil so here are a few libraries you can *choose* to use: 

- [Numpy](https://numpy.org/): A scientific computing package that helps with matrix multiplications, etc
- [Pandas](https://pandas.pydata.org/): Storing and manipulating data
- [Matplotlib](https://matplotlib.org/): Plotting the data when required. You can also use other plotting libraries if you prefer 
- Library of your choice for text pre-processing (lemmatization, tokenization, etc) such as [NLTK](https://www.nltk.org/). However, the training process should only take place on the neural network you have written from scratch. 
- [Gensim](https://radimrehurek.com/gensim/): Library to import and use word embeddings such as word2vec. 
- [Cuda](https://developer.nvidia.com/cuda-toolkit) or any library for utilising gpus for faster training times if you have access to a gpu. 

You don't *have* to use these libraries. They're only provided for your convenience.

## What is the problem and how to tackle it? 

### Building the Neural Network (Main Task)
The task is to build a simple feed forward neural network to predict customer rating from the reviews. You have to choose the architecture and hyper parameters for the network, i.e, number of layers, number of neurons, learning rate (if applicable) etc. 

There are a lot of resources to understand the inner workings of neural networks. Here are a few: 
- [Video](https://youtu.be/aircAruvnKk): the concepts behind how a neural network works 
- [Video](https://youtu.be/w8yWXqWQYmU): Building a neural network from scratch 
- [Series](https://youtube.com/playlist?list=PLQVvvaa0QuDcjD5BAw2DxE6OF2tius3V3): Neural networks from scratch

While writing the code for the neural network use Object Oriented Programming (OOP) concepts as and when required to make the code more robust to new use cases. For example, if you want to change the architecture of the neural network from having a single hidden layer with 50 neurons to a hidden layer with 100 neurons, it should be as simple as changing a parameter in a function from 50 to 100. Ex: as easy as changing `neural_network.layer(n=50)` to `neural_network.layer(n=100)`.

### Preparing the dataset 
The dataset provided is a modified version of the amazon cell phone reviews [dataset](https://www.kaggle.com/grikomsn/amazon-cell-phones-reviews?select=20191226-reviews.csv). It has three columns: 
- `rating`: this is the rating given (we are loosely think of this as sentiment)
- `title`: this is just a short version of the review 
- `body`: this is text of the actual full-length review 

Before you can train your neural network on this dataset you will have to go through a number of text pre-processing steps, some of which you can find [here](https://www.analyticsvidhya.com/blog/2021/06/text-preprocessing-in-nlp-with-python-codes/). Further you may have to use a word embedding to convert this text into a vector before you send it as input to your neural network. An example word embedding would be [**word2vec**](https://jalammar.github.io/illustrated-word2vec/) which can be found in the python library [**gensim**](https://machinelearningmastery.com/develop-word-embeddings-python-gensim/). 

You don't have to use the whole training dataset to train your model. reduce the training dataset size based on your computing power and time at hand. 

**Note**: In this whole section of data pre-processing you are allowed to use external libraries such as nltk, genesis, etc. to simplify the process. 

### Training, Validation and Results
You can use any portion of the `training-dataset.csv` for the purpose of training depending on the compute power accessible and time constraints. Once training is done, test your model on `testing-dataset.csv` and find the classification accuracy. 

## What are we looking for in the submission? 
Through this assessment we are trying to simulate a work environment where you are approached with a problem and a rough idea on what to do to solve it. The rest is up to you. You'll have to:

- Research about the problem and arrive at a theoretical solution 
- Go back to the whiteboard and sketch the architecture - define classes, functionalities, etc
- Convert your idea into code 
- Validate your solution and explain why it did or didn't go well and the challenges faced

We understand that this is a tough challenge, so don't worry if you're not able to complete it in time. The purpose of the assessment is to understand your learning speed and style, thought process, execution quality and clarity.   

If you have any doubts, queries or concerns feel free to reach out to me at `rana@maprecruit.ai`. 

Happy Coding!
