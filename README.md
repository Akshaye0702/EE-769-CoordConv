# EE-769-CoordConv
A repository for our EE769 project on stock market analysis using the coordconv network technique.

OBJECTIVE:
We plan to compare the effectiveness of 3 techniques for our project:
1) Vanilla CNN
2) CNNs with 1-D filter
3) CoordConv network

DATA:
We shall feed time series data in the form of the fractional change between the data on the current day D(i) and data from previous day D(i-1).This would be represented as an array of length (n-1) if we take the data of previous n days as our input.
For the CNN, we shall convert this array into a 2-D plot known as an Recurrence Plot (https://en.wikipedia.org/wiki/Recurrence_plot#:~:text=In%20descriptive%20statistics%20and%20chaos,phase%20space%20as%20at%20time%20.) And for the CoordConv network, we simply add coordinate data along with the plot as the input to the network.
Hypothetically, we do not expect much difference in performance between 1-D CNNs and CoordConv networks on the basis of input, as both are taking in the same time-series input in altered forms. Any difference in performance can be due to the way in the network stores information in its filters.

MODEL:
We will try to keep the number of trainable parameters and number of layers comparable between networks so the no one network can have any undue advantage. We will use the tensorflow and keras library to build all the networks and test them. We will tune the hyperparameters using gridsearchCV from the scipy library. 

ANALYSIS:
We shall compare results based on the Precision and Recall of the model test scores. We want a model which minimizes false positives and false negatives as these could lead to loss in stock market decisions. 
