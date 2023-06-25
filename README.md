
![steer](https://github.com/anujsahani01/Lane-Lines-Detection/assets/83875986/2eaff6f4-5438-474a-9fad-4b535c8051a5)

# Lane-Lines-Detection

## Encoder and Decoder architecture to extract main features from the images taken from each time frame from the video input and make predictions.

#### Working of the model:

Road Lane lines being one of the simplest features in the whole images makes it difficult to detect as the result a sharp change in intensity is detect as a lane.
In order to detect these simple features we use Semantic Segmentation(Image which is labeled for every pixel). In this model i have used Conv Nets for semantic segmentation these architecture are also known as U-Nets.
### U-Nets architecture: 
![image](https://github.com/anujsahani01/Lane-Lines-Detection/assets/83875986/70b1e1de-0b7e-4194-84c1-8d43fca669d5)


In this the image is first passed to encoder which helps in feature extarction then these extracted features are passed to decoder which again forms the image of the same size as input with the help of the extracted features(while encoding) this process lead to feature detection to the simplest level.


#### Plotting lane lines:
To draw the lanes i have used the following techniques:
1) used Sobel from opencv to blur the image
2) Used HoughLinesP to extract the edges and vertical lines from the region o fintrest
3) finally draw the lanes using an avg slope and intercept
The results after applying Unet arch on the segmented dataset are as follows:


## Loss and Accuracy
the model was trained for 100 epochs and the following results were obtained:

loss: 0.1821 - accuracy: 0.9479 - val_loss: 0.2078 - val_accuracy: 0.9440

