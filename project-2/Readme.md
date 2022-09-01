<!-- @format -->

# peoject to required to build

# requirements

The purpose of this assignment is to gain experience building and training neural networks. You will learn:

- Design and train a fully-connected neural network
- Train an existing CNN architecture using fine-tuning
- Visualize the trained model

### Submission Details

Submit your Jupyter notebook .ipynb file using Brightspace. Do not include any other files or images as they will not be reviewed.

<p>
<strong>Make certain that you run all the cells in the notebook you submit</strong> or you will loose marks.
</p>
<ul>
<li>You can submit multiple times, but only the most recent submission will be saved</li>
<li>Do not wait until the last minute to submit in case you have an unexpected issue</li>
<li>Review the late policy in the syllabus</li>
<li><strong>You must submit your own work</strong> and abide by the University of Ottawa policy on plagiarism and fraud</li>
</ul>

### DO NOT submit any images from the dataset

## Part 0. Data Preparation

To complete the assignment you will download the Caltech Bird dataset and devise an appropriate training set split. <b>You are free to sample from the dataset to reduce the overal training samples depending on your access to compute.</b> Again, the overall accuracy is less important than your observations and comparisons.

Dataset: <a href="http://www.vision.caltech.edu/visipedia/CUB-200-2011.html">Caltech-UCSD Birds-200-2011</a> (Also posed on Brightspace)

The dataset contains annotations for various tasks. In this assignment you will use the categories for classification (species labels)

In this section:

<ul>
<li>Download the dataset as described above</li>
<li>Create your splits for your dataset (there is a split provided for the full dataset) </li>
<li>Visualize five samples of each class by plotting a grid using the matplotlib library.</li>
</ul>

# Prepare your dataset here

## Part 1. Perceptron (3 Marks)

For this section you will implement a fully connected neural network (multi-layer perceptron). To do this you will need to perform the following steps:

- Resize the images to be no larger than 32x32.
- Use the sequential model API in keras to build your network using dense layers (consider performance impacts of fully connected layers)
- You must decide an appropriate number of neurons and layers.
- Print a summary of your model configuration.

When your classifier is working:

- Plot a loss curve for training and test data
- Plot an accuracy curve for training and test data
- Provide a brief discussion of your results

## Part 2. VGG-16 (4 Marks)

For this section you will adapt the VGG-16 network for the current task using tranfer learning and fine-tuning. You will implement the following in your process:

- You should choose a suitable image size.
- Choose a suitable labelling scheme.
- Use the pretrained VGG16 network available in Keras.
- Remove the top fully connected layers. Include your own FC layers that match our dataset.
- Choose some layers to "freeze" and the remaining layers you will fine-tune with the new dataset.

### Step 1

You will use the above steps to train a VGG-16 model using the Bird dataset

- Use transfer learning to train your first model by removing the FC layers, but leaving the other layers intact.
- Plot a loss curve for training and test data
- Plot an accuracy curve for training and test data

### Step 2

Now use the same steps as above, but this time unfreeze some convolutional layers and retrain the network. Again, plot your results.

### Step 3

Discuss the results of both methods from step 1 and step 2 while using plots and graphics to support your discussion.

## Part 3. Visualization (3 Marks)

For this section you will visualize the filters learned byyour VGG-16 network and use t-SNE to observe clusters that were learned by your model.

- Make sure to provide the graphic results for your visualizations
- Provide an interpretation of the results

## Bonus (1 Mark)

Visualize the activation maps produced by your network and discuss the results using an image from the test test and another image of your choice.
