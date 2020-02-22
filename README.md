# GA + NN (Genetic Algorithm with fitness function represented by CNN)

The main idea of this research is to combine **genetic algorithms (GA)** with **neural networks (NN)** by setting a NN as a fitness function of the GA. In this case, I decided to try CNN and images of cats. The final result of this work should be a GA which uses CNN as a fitness function to generate pictures of cats from random white noise. **!WARNING! WORK IS STILL IN PROGRESS !WARNING!**  

## What is GA? 

The answer to this question you can find in **GA.ipynb**. There is a simple GA realization in this Jupyter Notebook with DNA class representing an object of the total population that combines with other similar objects to create the next population better. This Jupyter Notebook recreates a certain string from the random text of the same length.

## First step - CNN traning

Fist of all we need to train a model. **CNN_training.ipynb** notebook contains steps of CNN classifier training, its main goal is to distinguish cats picture from random white noise. **Note:** This notebook also contains a ResNet-based model training and CNN debugging visualization technique.

## Second step - GA creation

The next step was to modify **GA.ipynb** so that instead of a string the DNA object will represent an image. **GA_NN.ipynb** contains the combination of CNN and GA where after every 10 iterations 3 best population members are displayed. At the end of the file, there is a cell in which you can visualize your own photo.

## Parameters of GA, link to datasets

Here are the common parameters for the GA:
```
mutation_rate = 0.0004
total_population = 1000
relief = 0.01
survived_parents = int(total_population * 0.04)
num_of_iterations = 7000
```
**Note:** You may try to run algorithm without mutations (mutation_rate = 0).

Also, you can find cats dataset with label [here](https://drive.google.com/drive/folders/18h6H6pXqndlszwpUmjQZY2aPstsiG3JB?usp=sharing). By this link, you also can find a dataset of people's faces but keep in mind that these pictures **have 3 channels**.


