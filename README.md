# PA#3

## Name: Nissi ALeichem B. Sulit
## Section: 2ECE-B
## Date Submitted: September 10, 2026

The experiment focuses on loading a CSV dataset into a Pandas DataFrame, selecting rows and columns using positional and label-based indexing, filtering records with Boolean conditions, and extracting specific data subsets without modifying the original dataset. The cars.csv dataset is used throughout the activity.

## Problem A: Positional and Label-Based Slicing

This problem involves performing positional and label-based slicing on the cars DataFrame. First, the CSV dataset is loaded into a DataFrame named cars. The shape and complete list of column names are then displayed to provide an overview of the dataset.

```python
import pandas as pd
cars = pd.read_csv("cars.csv")


````
