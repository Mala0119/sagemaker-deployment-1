# SageMaker Deployment Project - AI Engineering Udacity Nanotrack

This is the final solution of the project 'Sagemaker Deployment' which consists in deploying a Sentiment Analysis model using XGBoost in the Amazon AWS SageMaker tool. The notebook and Python files provided here result in a simple web app which interacts with a deployed recurrent neural network performing sentiment analysis on movie reviews.

In the final architecture AWS API Gateway and AWS Lambda functions is used as well. The application architecture diagram is:

![Web app Diagram](./Web&#32;App&#32;Diagram.svg) 

You can find the original code without solutions in the original [Udacity SageMaker Deployment repository](https://github.com/udacity/sagemaker-deployment).

 This project assumes some familiarity with SageMaker, the IMDB Sentiment Analysis using XGBoost mini-project (which can be found in the original repository) should provide enough background.


## Setup instructions
Please see the [original README](https://github.com/udacity/sagemaker-deployment/tree/master/README.md) in the root directory for instructions on setting up a SageMaker notebook and downloading the project files (as well as the other notebooks). For the solutions only clone this repository:

## Project Overview

In this project, I have used Amazon SageMaker to complete an entire lifecycle of a machine learning project. The goal is to build a very simple web page in which a user can submit a movie review and the prediction model behind the scenes will predict whether it is Positive or Negative review. The prediction model is implemented using Pytorch framework and trainned on IMDB dataset.


## Project Instruction

This entire project is done on Amazon sagemaker and uses some heavy GPU instances for training the models. If you want execute this on local machine, you might want to train the model on subset of the training data from IMDB dataset. Also there are steps where we upload the data to amazon S3 instances in order to train using aws instances which you can totally ignore on local machines

### Instructions to execute in sagemaker
```
1. Clone the repository.
	```
		git clone https://github.com/Mala0119/sagemaker-deployment-1.git
	```
2. Open the `SageMaker Project.ipynb` file.
	```
		jupyter notebook SageMaker Proejct.ipynb
	```
3. Read and follow the instructions! You can find and download the dataset for this project in the notebook.
```
### General Outline

- Step 1: Downloading the data
- Step 2: Preparing and Processing the data
- Step 3: Upload the data to S3
- Step 4: Build and Train the PyTorch Model
- Step 5: Testing the Model
- Step 6: Deploying the model for testing
- Step 7: Use the model for testing
- Step 6  Deploy the model for the web app
- Step 7  Use the model for the web app

### Libraries

The list below represents main libraries and its objects
for the project.
- [Amazon SageMaker](https://ap-northeast-2.console.aws.amazon.com/sagemaker/home?region=ap-northeast-2#/landing) (Build, train, and deploy a model)
- [PyTorch](https://pytorch.org) (LSTM classifier)

### Delete the Endpoint
Remember to always __SHUT DOWN YOUR ENDPOINT__ if you are no longer using it. You are charged for the length of time that the endpoint is running so if you forget and leave it on you could end up with an unexpectedly large bill.
```
	predictor.delete_endpoint()
```