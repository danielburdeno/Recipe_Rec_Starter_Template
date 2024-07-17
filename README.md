# Recipe Search and Recommendation Starter Repo

![recipe image](images/header.jpg)

Author: Daniel Burdeno -- Lead Data Science Instructor -- Flatiron School

## Overview

This repository can be used as a starting base to follow along for a streamlit demo/lesson using a recipe dataset to produce recipes based on ingredient and tag selection as well as conduct basic content similarity comparison and recommendation. In this reposistory are provided data files and a requirements file in order to reproduce the python coding environments

## Environment Setup

Anaconda or a similar environment and package manager will be need to setup. Streamlit utilizes pip to setup and install dependicies via it's cloud platform so will be using a requirements.txt file to document and denote package and environment information.

To setup the corresponding environment via conda:
- Step 1: Create environment with pip (feel free to give it a different name)
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