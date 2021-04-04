# README - Computer Vision City Classifier

## Overview

This Computer Vision program receives a street-level picture and is able to predict the city it has been shot in.

## The Data

We used a not public database called [Mapillary](https://www.mapillary.com/), for which we have been granted a special academic permission.


The database had initially a total of 1.5 million pictures and it was imbalanced over the 19 different cities.

The pictures have been shot every few seconds from some vehicles moving through the streets of the cities, pretty much like Google Maps.

This is why we decided to keep only one frame every 80 in order not to have overfitting on the particular characteristics of some streets and on particular vehicles that could have stayed in front of the camera for a while, showing up in 40 frames in a row for example.

After this reduction we undersampled in order to balance the dataset, resulting in 1000 images per city.

Moreover, we noticed that in the lower part of every picture the dashboard of the vehicle was visible, and this would have damaged the quality of the algorithm, generating a bias on the particular vehicle model, so we cropped off a rectangle from the lower part of every picture.

## Algorithm

As a first step, we started out with a classification model based on 3 cities: Paris, Goa and Sao Paulo. We observed the quality of a baseline model such as Random Forest and the improvement obtained through the implementation of a deep learning model. Predicting on the pictures test set, the accuracy witnessed a raise from 80% to 95% thanks to Google's LeNet transfer learning.

Thrilled by the results, we enriched the program with various additional steps: not only enlarging the dataset to 19 cities, but also performing an Anomaly Detection through Autoencoders, resulting in an overall accuracy rate of 91% on the 19 cities application, predicting on the test set.

Moved by insatiable curiosity, we exploited the lime interpreter package in order to have a better clue of the criteria with which the various sections of the images influence the algorithm, and not tired after all this, we had some fun attempting a GAN generation in order to fulfil the dream of a hybrid city, with, for example, the streets of Berlin, the architecture of Paris and the traffic lights of San Francisco. Don't worry, you will find the results of this experiment on our application webpage.

Lastly, we felt the need to deliver some interactive and enjoyable product to the world, and therefore we deployed, thanks to Heroku, a web application able to perform the prediction on an arbitrary image, not taken anymore from the test set, but from Google Street View for example.

## Usage

If you want to try out the web application, uploading a street-level picture randomly captured with Google Street View, while having a look at the GAN generated images in the meantime, just click on the [link](https://cities19test.herokuapp.com/) and have fun!

## Created by:
- `Daniel Saban`
- `Sagi Elfassi`
- `Arad Ben Haim`
- `Itamar Bergfreund`
- `Dor Meir`
