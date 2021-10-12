# Sudoku-Solver
## Hold the image in front of the camera like this:
![image](https://user-images.githubusercontent.com/55214244/135301365-378b8899-6890-495f-b642-7d6dc77b9cf4.png)


## MAIN STEPS INVOLVED

1) Processing of the Sudoku grid

2) Recognition of Digits

3) Solving the puzzle

### STEP1: PROCESSING OF THE SUDOKU GRID INVOLVES-

1. Converting the image clicked into greyscale image.

2. Blur the image using Gaussian Bluring .

3. Apply Adaptive Thresholding . We get a Binary Image.

4. Find all the contours.

5. Extract the contour with biggest area.

6. Locate 4 corners of the contour and determine the upper left ,
upper right, bottom left, bottom right corners.

Use 2 criteria for qualifying a sudoku grid: 4 angles must be
approximately 90 degrees. 4 sides must have approximately equal
lengths.

If the biggest contour is a square, apply cv2.warpPerspective get
a nice and stable Sudoku Grid Image.

## STEP2 : DIGIT RECOGNITION

### Steps Involved are:

1) Image pre-processing,

2) Training a Convolutional Neural Network model to
classify the digits.
### Our dataset consists of a subset of Chars74k dataset:

We used a Conventional Neural Network(CNN) to train our dataset

Now after splitting the dataset into 80% training and 20% test, both the
training and test dataset has gone following transformations:

Data type has changed to float32.

Pixels are normalized to 0 and 1 by dividing each pixel by 255.

Now a neural network architecture is made for the data. Softmax
Activation function is used for output layer and relu Activation Function
is used for non output layers. After this model is created, our training set is
compiled and fit into the model.

Greedy best-first search algorithm always selects the path which
appears best at that moment.

## Final results will be like this
![image](https://user-images.githubusercontent.com/55214244/135299657-b9631f9a-b8ec-4a58-a5bd-cce933219d2b.png)
