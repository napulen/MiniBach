# MiniBach
Implementation of the MiniBach model described in the book *Deep Learning Techniques for Music Generation*.

----
## About

The `MiniBach` model is very simple (a feedforward network with only one hidden layer) so it can be considered a kind of **Hello World** for symbolic music generation. It is perfect for people just starting with deep learning. For the *not so beginners* on deep learning, maybe the encoding of the music score provides some insight. In any case, I couldn't find an implementation of the model when I saw it on the book, and decided that it would be a nice contribution to the community.

----
## Code

The implementation is written in a tutorial-like fashion spread out in four notebooks:
- **Part 1**: Taking a collection of `Humdrum **kern` symbolic music files (Bach chorales) and process them into 4-measure chunks of training data
- **Part 2**: Encoding the 4-measure chunks of training data into one-hot-encoded vectors for the neural network, separating the soprano (input) from the three lower voices (output)
- **Part 3**: Training the neural network and predicting the accompaniment for one of the melodies in the training examples
- **Part 4**: Generating the accompaniment for an arbitrary melody

If cloning the repository, clone recursively to get the submodule with the Bach chorales, which are provided by [Craig Sapp](https://github.com/craigsapp/bach-370-chorales):
```
git clone https://github.com/napulen/MiniBach.git --recursive
```

----
## Requirements

The music processing is done using [music21](http://web.mit.edu/music21/). The network is implemented with `tensorflow`, and `pandas` dataframes are used a few times. 

----
## Source

More details about this and other (more advanced) models can be found in the book:

Briot, Jean-Pierre, Gaëtan Hadjeres, and François Pachet. 2017. “Deep Learning Techniques for Music Generation - A Survey.” CoRR abs/1709.01620. http://arxiv.org/abs/1709.01620.

----
Enjoy!
