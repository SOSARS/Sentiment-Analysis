# Sentiment-Analysis
A simple sentiment analysis task that analyses Amazon book reviews. Involved in the project is a Recurrent Neural Network developed and trained to identify whether an Amazon book review is positive or negative based on the semantics of the review. 

The first steps taken involve the pre-processing of the reviews. Positive and negative reviews are stored in different text files. Both text files are read into a single list. Two labels identifying "positive" and "negative" reviews are appended as well and the respective reviews are appended to the list. The labels are then converted to a categorical ([1, 0] - positive or [0, 1] - negative) form to input into the neural network for training and prediction generating. 

Additional exploration is conducted to identify the average length of the reviews, the standard deviation and the number of unique words found in all of the combined reviews. The reviews are then tokenised (converted to numerical values) in the list of combined reviews. Once the data is tokenised, additional padding is conducted on the dataset to make all reviews a maximum length of four words using the Keras pad_sequences function. 

The data is then split into training and testing sets (80% training and 20% testing) and the model is constructed by adding a Long Short Term Memory layer, a Batch Normalisation layer, Embedding layer, Dense layer with a 'softmax' activation function and a SpatialDropout1D layer. Once the model is constructed, the training data is then fitted to the model to generate predictions. A confusion matrix is created to identify True Positives, False Positives, True Negatives and False Negatives, a visual representation of the performance of the newly trained model. 

Model scores are then produced along with the performance of the model, measuring accuracy against the rate of loss per epoch. Results are then generated with a performance result of 80%. 
