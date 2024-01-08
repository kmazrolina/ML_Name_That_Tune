# Name That Tune: Jaka to kolęda?
### JiBAD Projekt Zaliczeniowy
#### Karolina Źróbek

## Overview

The repository contains a project focused on classifying Polish Christmas Carols (kolędy) based on chroma features extracted from melodies. The project structure includes the following:

- **Carol_Classifier**: Main directory containing the Python scripts and Jupyter notebooks related to the project.
  - `Carol_Classification-Melody_Extracts.ipynb`: Jupyter notebook for the classification of songs with highlighted main melody.
  - `Carol_Classification-Original_Songs.ipynb`: Jupyter notebook for the classification of original songs.
  - `ChromaCoverId`: Component related to chroma feature extraction cloned from [here](https://github.com/albincorreya/ChromaCoverId).
  - `Data_prep.ipynb`: Jupyter notebook focusing on data preparation.
  - `Melody_extractor.ipynb`: Jupyter notebook dedicated to main melody extraction.
  - `koledy`: Directory storing the dataset of Polish Christmas Carols.
  - `validation_data`: Directory containing validation data.

- **requirements.txt**: Lists the project dependencies. Install them using `pip install -r requirements.txt`.


This project aims to classify music based on structural features, specifically focusing on melodies independent from key or tempo. The primary focus is on Polish Christmas Carols (kolędy). The approach is based on three key references [Serra et al. (2009)](https://iopscience.iop.org/article/10.1088/1367-2630/11/9/093017), [Chen et al. (2017)], [ChromaCoverId](https://github.com/albincorreya/ChromaCoverId/) by @albincorreyathat contribute to the understanding and methodology used in the project.

## Problem Statement

The aim is similar to Cover Song Identification, which involves the classification of music based on its structural elements, particularly melodies. The goal is to distinguish between different versions of the same song performed by various artists while disregarding factors such as key or tempo variations.

## Results

The project has yielded following results based on the two approaches:

1. **Model Trained on Melody Extracts:**
   - **Accuracy:** ~73%
   - The model performs moderately well and exhibits lower accuracy compared to the model trained on original versions of the Christmas carols.
   
2. **Model Trained on Original Versions:**
   - **Accuracy:** ~89%
   - This model outperforms the melody-only approach, emphasizing the importance of considering the complete musical structure.

## Challenges and Insights

1. **Generalization to New Data:**
   - The model, particularly the one trained on melody extracts, does not generalize well to new data. Performance diminishes when applied to songs performed by artists not included in the training dataset.
   - Chroma feature extraction may be influenced by additional factors such as music genre, accompaniment, or voice timbre.

2. **Overfitting:**
   - While achieving high accuracy for various interpretations of Polish Christmas carols, the model seems overfitted.
   - Poor predictions for samples performed by artists outside the training dataset suggest a need for robustness against diverse musical styles.

