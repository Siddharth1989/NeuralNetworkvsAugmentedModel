# NeuralNetworkvsAugmentedModel
In this project, we are computing and comparing the reconstruction error and classification errors of a 3-Layer Neural Network Model and an Augmented Feature Model<br>
We have three datasets:<br>
1. The labelled and unlabelled datasets are used to train the autoencoder.
2. The labelled dataset is used to train the classifier.
3. The test dataset is used to validate the trained classifier.

The following steps were implemented for this project:
1. The autoencoder was trained with only one hidden layer with the number of neurons from 30 to 360 with a step size of 30.
2. For each model, the reconstruction error is computed. The reconstruction error is the average of Euclidean distances between the input and output of the autoencoder. Furthermore, these values were plotted with the number of units in the middle layer on the x-axis and the reconstruction error on the y-axis.
3. Next, a 3-layer Neural network was built to build a classification model with the original attributes from the training set and the number of neurons was set from 30 to 360 with a step size of 30. The test error was calculated and recorded for each model.
4. An augmented self-taught network was built with the autoencoder models as follows:
   1. The output of the middle layer of the autoencoder was added as extra features to the feature set.
   2. The 3-layer neural network was trained with all the features (original + extra) and by varying the number of neurons as mentioned in step 3. Finally, the test error was calculated and recorded.
      For example, each model was developed as follows:<br>
           (i) Model 1: 30 hidden neurons + extra 30 features (from an autoencoder)<br>
           (ii) Model 2: 60 hidden neurons + extra 60 features (from an autoencoder), ...,<br>
           (iii) Model 20: 360 hidden neurons + extra 360 features (from an autoencoder)
5. The error rates were plotted for the 3-layer neural networks from step 3 and the augmented self-taught network from step 4, with the number of hidden neurons on the x-axis and the classification error on the y-axis.

Instructions:<br>
Please use the appropriate references in line with the GNU General Public Licence 3.0 while reusing this code.
