# Kaggle Digit Recognizer

## Overview

The goal in this competition is to take an image of a handwritten single digit, and determine what that digit is.
For every in the test set, you should predict the correct label.

## Table of Contents

- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Model Development](#model-development)
- [Model Evaluation](#model-evaluation)
- [Conclusion](#conclusion)
- [References](#references)

## Dataset

Reference the data [here](https://www.kaggle.com/competitions/digit-recognizer/data)

The data files train.csv and test.csv contain gray-scale images of hand-drawn digits, from zero through nine.

Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255, inclusive.

The training data set, (train.csv), has 785 columns. The first column, called "label", is the digit that was drawn by the user. The rest of the columns contain the pixel-values of the associated image.

Each pixel column in the training set has a name like pixelx, where x is an integer between 0 and 783, inclusive. To locate this pixel on the image, suppose that we have decomposed x as x = i * 28 + j, where i and j are integers between 0 and 27, inclusive. Then pixelx is located on row i and column j of a 28 x 28 matrix, (indexing by zero).

For example, pixel31 indicates the pixel that is in the fourth column from the left, and the second row from the top, as in the ascii-diagram below.

## Data Preprocessing

For this competition we evaluate first if the data is normalized, then we perform the scaled normalization based on the max value, 255 in this case due to pixel max values in each channel (RGB) 

## Exploratory Data Analysis (EDA)

Conducting exploratory data analysis to gain insights into the dataset. This dataset provides a straightforward EDA given that there are not outliers or missing values, visualization wasn't performed during EDA because data was well known.

## Model Development

For this challenge we are using tensorflow's Dense layers, an input with 128 nodes and a relu activation function, this because the consistency in the shape of the data. then, we provide a hidden Dense layer with 128 nodes and other relu activation function, finally we set a Denser layer with softmax activation function. 

For regularization we use DropOut layers.

## Model Evaluation

Currently the accuracy of the model is 0.97287 (97%) with position 1093 in the [leaderboard](https://www.kaggle.com/competitions/digit-recognizer/leaderboard)
 
## Conclusion

With this Kaggle challenge we've introduced the necessary skills to use tensorflow's tools for computer vision, the most basic ones and also how to submit results into Kaggle competitions.


## References

* [Competition](https://www.kaggle.com/competitions/digit-recognizer/overview)
* [Example 1](https://www.kaggle.com/code/poonaml/deep-neural-network-keras-way)
* [Example 2](https://www.kaggle.com/code/fchollet/simple-deep-mlp-with-keras/code)
