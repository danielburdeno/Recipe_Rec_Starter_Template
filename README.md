# Recipe Search and Recommendation Starter Repo

![recipe image](images/header.jpg)

Author: Daniel Burdeno -- Lead Data Science Instructor -- Flatiron School

## Overview

This repository can be used as a starting base to follow along for a streamlit demo/lesson using a recipe dataset to produce recipes based on ingredient and tag selection as well as conduct basic content similarity comparison and recommendation. In this reposistory are provided cleaned data files and a requirements file in order to reproduce the python coding environment.

## Environment Setup

Anaconda or a similar environment and package manager will be need to setup. Streamlit utilizes pip to setup and install dependicies via it's cloud platform so we will be using a requirements.txt file to document and denote package and environment information.

To setup the corresponding environment via conda:
- Step 1: Create conda environment containing pip (feel free to give it a different name)
```
conda create --name recipe_st_env pip
```
- Step 2: Activate new environment
```
conda activate recipe_st_env
```
- Step 3: Use the provided requirements.txt file to install via pip
```
pip install -r requirements.txt
```

## Data Understanding

The data for this demo comes from a Kaggle dataset of over 230,000 recipes pulled from [Food.com](https://www.food.com/?ref=nav) (formerly GenuisKitchen). I utilized the RAW_recipes.csv file for our purposes here.

[Kaggle Dataset](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions?resource=download&select=RAW_recipes.csv)

The archive zip folder should be downloaded and extracted. The RAW_recipes.csv file can then be moved into the data folder within this repository in order to run the data_cleaning notebook file.

I have provided parquet files resulting from the data_cleaning notebook within the repository for ease of use. They are provided as parquet files and split up into three seperate files due to github file size limitations. 

- **recipes_ingtag**: File contains the tags and ingredients as list objects for each recipe 
    - Primary file used for ingredient and tag seach matching
    - Contains recipe id to match with other files

- **recipes_steps**: File contains recipe name, cooking steps, and a description of the recipe
    - Primary file used to return recipes to a user in order to display steps and description
    - Contains recipe id to match with other files

- **recipes_feat**: File contains content information about each recipe including common tags and ingredients
    - Primary file used to create vector similarity for content based recommendation
    - Contains recipe id to match with other files

This kaggle dataset contains a lot of other good information pertaining to user interations with Food.com and the associated recipes which can be used in more advanced analysis and recommendations based on user preference (collaborative filtering and beyond). This information was not used here.
