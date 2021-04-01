# README - Computer Vision City Classifier

## Overview

This Computer Vision program receives a street-level picture and is able to predict the city it has been shot in.

## The Data

We used a not public database called [Mapillary](https://www.mapillary.com/), for which we have been granted a special academic permission.


The database had initially a total of 1.5 million pictures and it was imbalanced over the 19 different cities.

The pictures have been shot every few seconds from some vehicles moving through the streets of the city, pretty much like google maps.

This is why we decided to keep only one frame every 80 in order not to have overfitting on the particular characteristics of some streets and on particular vehicles that could have stayed in front of the camera for a while, showing up in 40 frames in a row for example.

After this reduction we undersampled in order to balance the dataset, resulting in 1000 images per city.

Moreover, we noticed that in the lower part of every picture the dashboard of the vehicle was visible, and this would have damaged the quality of the algorithm, generating a bias on the particular vehicle model, so we cropped off a rectangle from the lower part of every picture.

## Algorithm

## Usage


## Created by:
- `Arad Ben Haim`
- `Daniel Saban`
- `Itamar Bergfreund`
- `Dor Meir`
- and
- `Sagi Elfassi`

ADIDaS!
