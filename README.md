"# Lane-Lines-Detection" 

In this I have used Encoder and Decoder architecture to extract main features from the images taken from each time frame from the video input.

The results after applying Unet arch on the segmented dataset are as follows:

loss: 0.1821 - accuracy: 0.9479 - val_loss: 0.2078 - val_accuracy: 0.9440
the model was trained for 100 epochs

To draw the lanes i have used the following techniques:
1) used Sobel from opencv to blur the image
2) Used HoughLinesP to extract the edges and vertical lines from the region o fintrest
3) finally draw the lanes using an avg slope and intercept
