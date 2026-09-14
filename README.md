# PA#3

## Name: Nissi Aleichem B. Sulit
## Section: 2ECE-B
## Date Submitted: September 10, 2026

The experiment focuses on loading a CSV dataset into a Pandas DataFrame, selecting rows and columns using positional and label-based indexing, filtering records with Boolean conditions, and extracting specific data subsets without modifying the original dataset. The cars.csv dataset is used throughout the activity.

## Problem A: Positional and Label-Based Slicing

This problem involves performing positional and label-based slicing on the cars DataFrame. First, the CSV dataset is loaded into a DataFrame named cars. The shape and complete list of column names are then displayed to provide an overview of the dataset.

```python
import pandas as pd

cars = pd.read_csv("cars.csv")

# Required Checks
print("Shape of cars:")
print(cars.shape)

print("\nColumn names:")
print(cars.columns.tolist())

cars_6_to_10 = cars.iloc[5:10]

# Select required columns using column labels
cars_6_to_10_selected = cars_6_to_10[["Model", "mpg", "cyl", "hp", "gear"]]

print("\nCars 6 to 10:")
print(cars_6_to_10)

print("\nSelected columns from cars 6 to 10:")
print(cars_6_to_10_selected)


````
## Problem B: Model Lookup

This problem involves using Boolean indexing to locate specific vehicle models in the cars DataFrame. Instead of using hard-coded row numbers, the Model column is used as the condition for finding the requested records. For this part, the complete row corresponding to the Toyota Corolla is stored in a variable named toyota. For the second part, the record for Pontiac Firebird is stored in Pontiac, while only the Model, mpg, hp, and wt columns are retained. Both results are created as new subsets without changing the original cars

```python
# Toyota Corolla
toyota = df.loc[df['Model'] == 'Toyota Corolla']

print("Toyota Corolla:")
print(toyota)

# Pontiac Firebird
pontiac = df.loc[
    df['Model'] == 'Pontiac Firebird',
    ['Model', 'mpg', 'hp', 'wt']]

print("\nPontiac Firebird:")
print(pontiac)

````

## Problem C: MULTI-MODEL SUBSETTING

This problem requires creating a new DataFrame containing only three specific vehicle models: Datsun 710, Lotus Europa, and Ferrari Dino. The rows are selected based on their model values rather than their row numbers.

```python

models = ["Datsun 710", "Lotus Europa", "Ferrari Dino"]
selected_cars = cars[cars["Model"].isin(models)][["Model", "mpg", "cyl", "hp", "gear"]]

print("Selected cars:")
print(selected_cars)

print("\nShape of selected_cars:")
print(selected_cars.shape)

````
