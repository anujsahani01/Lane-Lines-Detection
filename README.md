
![steer](https://github.com/anujsahani01/Lane-Lines-Detection/assets/83875986/2eaff6f4-5438-474a-9fad-4b535c8051a5)

# Lane-Lines-Detection

## Encoder-Decoder Architecture for Lane Line Extraction:

The task of detecting road lane lines in images is challenging due to their simplicity and the presence of various image artifacts. One effective approach to tackle this problem is by employing semantic segmentation, which involves labeling each pixel in an image. In this project, a Convolutional Neural Network (CNN) architecture called U-Net is used for semantic segmentation.

### U-Net architecture: 

U-Net is a popular architecture for image segmentation tasks. It consists of an encoder and a decoder network, which work in tandem to extract essential features from the input images and make predictions.

The architecture diagram of U-Net can be visualized as follows:
![image](https://github.com/anujsahani01/Lane-Lines-Detection/assets/83875986/70b1e1de-0b7e-4194-84c1-8d43fca669d5)


The input image is first passed through the encoder, which helps in extracting informative features. These features are then propagated to the decoder block, which reconstructs an image of the same size as the input. By utilizing the extracted features during encoding, this process enables the detection of lane lines at a simple feature level.


#### Plotting lane lines:

To draw the detected lane lines, several techniques are employed:

1) Sobel Filter: The input image is convolved with the Sobel filter, which helps in blurring the image and enhancing edges.

2) HoughLinesP: The edges and vertical lines are extracted from a specific region of interest using the HoughLinesP algorithm. This step further refines the lane line detection.

3) Drawing Lanes: The detected lanes are drawn using the average slope and intercept values obtained from the HoughLinesP output.

## Loss and Accuracy
The U-Net model was trained for 100 epochs, and the following results were achieved:

* Training Loss: 0.1821
* Training Accuracy: 0.9479
* Validation Loss: 0.2078
* Validation Accuracy: 0.9440


During training, the model iteratively learned to minimize the loss function and improve its accuracy in predicting lane lines.

By leveraging the power of U-Net architecture and combining it with image processing techniques, the model achieved impressive results in lane line detection. The trained model can now accurately identify and plot the lane lines in road images, providing valuable information for various applications such as autonomous driving and road maintenance.

## Feedback

If you have any feedback, please reach out to me at: [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/anuj-sahani-34363725b) 

Author: [@anujsahani01](https://github.com/anujsahani01)

