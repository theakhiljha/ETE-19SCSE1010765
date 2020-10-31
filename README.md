#### NAME- AKHIL KUMAR JHA
#### ADMISSION NO.- 19SCSE1010765
#### ENROLLMENT NO. - 19021012093
#### BATCH- CSE-5/ML-2
#### SEMESTER- 5
#### YEAR- 3
#### GITHUB URL: https://github.com/theakhiljha/ETE-19SCSE1010765

## Ques 6: Write a program to implement k-Nearest Neighbour algorithm to classify the iris data set. Print both correct and wrong predictions.

# K-Nearest Neighbor (KNN)

KNN is simple supervised learning algorithm used for both regression and classification problems it basically stores all available cases and classify new cases based on similarities with stored cases.

kNN calculates the distance between data points. For this , we use the simple Euclidean Distance formula.

![title](https://i.ibb.co/gmDRz9N/1-BQJFF3ckt-R-Kn32v-M4-Cme-Q.png)

k = Number of nearest neighbours

    k=1 - The training data is in the same level of the closet example provided in the training set.
    k=4 - The most common class from the four closet classesa are assigned to the testing data. 
    
### What KNN Algorithm Does?


1. Load the data
2. Initialize K to your chosen number of neighbors
3. For each example in the data
    3.1 Calculate the distance between the query example and the current example from the data.
    3.2 Add the distance and the index of the example to an ordered collection
4. Sort the ordered collection of distances and indices from smallest to largest (in ascending order) by the distances
5. Pick the first K entries from the sorted collection
6. Get the labels of the selected K entries
7. If regression, return the mean of the K labels
8. If classification, return the mode of the K labels

### The Right Value For K.

To select the K that’s right for our data, we run the KNN algorithm several times with different values of K and choose the K that reduces the number of errors we encounter while maintaining the algorithm’s ability to accurately make predictions when it’s given data it hasn’t seen before.

1. When we decrease the value of K to 1, our predictions become less stable.
2. Inversely, as we increase the value of K, our predictions become more stable due to majority voting / averaging, and thus, more likely to make more accurate predictions (up to a certain point).
3. In cases where we are taking a majority vote (e.g. picking the mode in a classification problem) among labels, we usually make K an odd number to have a tiebreaker.

#### Advantages

1. The algorithm is simple and easy to implement.
2. There’s no need to build a model, tune several parameters, or make additional assumptions.
3. The algorithm is versatile. It can be used for classification, regression, and search (as we will see in the next section).

#### Disadvantages

The algorithm gets significantly slower as the number of examples and/or predictors/independent variables increase.
