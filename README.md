# COVID-19 Pneumonia Detection using CNN

The novel CoronaVirus (COVID-19) has infected millions of people around the world. This pandemic has not only infected people and taken the lives of lakhs, but also affected people’s life in a really harsh manner where-in all trivial daily activities have become a luxury. It has infected over a million people in the US and the death toll is very high. This pandemic has taken a big toll on the medical community. The nurses and doctors are the ones whose life has been affected the most. The purpose of this project is to help the global medical community in easing their work through Machine Learning and make the process of COVID-19 Pneumonia diagnosis faster and error free, in order to avoid false negatives and save the lives of many by providing quick treatment.

COVID-19 affects the respiratory system of the human body, and one of its complications is the  pneumonia that is caused due to it, which can be life threatening. This pneumonia is detected using the X-rays of the patients. However, the difference between COVID-19 pneumonia and viral pneumonia is very difficult, even for medical experts to scan visually.
To help eliminate this problem, we aim to build a Deep Learning model that distinguishes the x-ray images as COVID-19 pneumonia, viral pneumonia and a healthy patient. To implement this, we have used Convolution Neural Networks (CNN) on the patient's chest X-Ray images.

### Data
We used the COVID-19 radiography dataset from [kaggle](https://www.kaggle.com/tawsifurrahman/covid19-radiography-database). The dataset is open source and can be used by anyone. It contains chest x-ray images of patients. The data is formatted such that it contains folders for each of the three classes and metadata files giving attributes of the data such as name, file type(PNG), file path and image size in pixels. The dataset does not have any CSV file with image data along with their labels.
The dataset contains 219 images of COVID-19 patient’s lungs, 1341 images of healthy patient’s images and 1345 images of viral pneumonia patients. These images are 1024 X 1024 pixels with all three channels that are RGB.

The normal, viral and COVID images look like this:

![screenshots/plot_images.png](screenshots/plot_images.png?raw=true)


### Execution
The project has a Google Colaboratory Notebook [**COVID_19_project.ipynb**](https://github.com/utsav-195/covid-19-detection-using-cnn/blob/master/COVID_19_Project.ipynb) which is used for the implementation of this project.
There is an option to open the notebook in google colab directly from the notebook.
The reason to use Google Colaboratory is that it provides GPU for use which helps in training complex deep learning models on images much faster than standard CPUs.
The Jupyter notebook has explainations as to what each cell does.
Run each cell and you can observe the output of the commands.

### Challenges
Class Imbalance: The number of images for the COVID-19 affected lungs were way less than other classes. This imbalance was overcome by using data augmentation techniques on the COVID-19 images.

Model Selection: A lot of literature review went under to select which models will be suitable for our data and the problem we are trying to solve.

Parameter Tuning: The Convolutional Neural Networks have a variety of parameters that can be used to make our model fit better on the data provided. The parameters which we experimented with were the number of fully connected layers, the number of nodes in each layer, optimizer, it's learing rate, dropout, regularization, etc.
A lot of experiments were done with these parameters to give the acquired accuracy.

### Results
The results of our experiments and approach are below:

![screenshots/results.png](screenshots/results.PNG?raw=true)

Overall it was a fun project to work on which lead to immense learning!
We plan to continue working to acquire a 99.999% accuracy.
You can download the weights of the best model that is VGG-19 [here](https://drive.google.com/open?id=1XDp5d-0cMwe9g5vazY5CGGolqCQXSlt2).

**Note:** More detailed information/report can be found in the [Project Report.pdf](https://github.com/utsav-195/covid-19-detection-using-cnn/blob/master/Project%20Report.pdf).
