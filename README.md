The project involves assessing coral reef fish species using a dataset that includes:

- **Fish species density data**: Information about the density of 109 fish species across various survey sites.
- **Environmental data**: Variables that could affect fish density, such as coral cover, reef complexity, sea surface temperature, net primary productivity, wave exposure, habitat types, and anthropogenic factors.
- **Trait data**: Morphological, behavioral, and ecological traits of the fish species, including their response variables associated with relief (structural complexity of reefs) and coral cover.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Conclusions](#conclusions)

## Installation
*Python Version: 3.11.7*
1. Clone the repository
    ```sh
    git clone https://github.com/gpealat/coralreef
    ```
2. Change into the project directory
    ```sh
    cd coralreef
    ```
3. (Recommended) If you are using anaconda, create a virtual environment first
    ```sh
    conda create --name coral
    ```
4. (Recommended) Activate the virtual environment
      ```sh
      conda activate coral
      ```
5. Install the required packages
    ```sh
    pip install -r requirements.txt
    ```
6. Run Jupyter
   ```jupyter notebook```

## Usage

Run each of the notebooks in the following order

1. [EDA](https://github.com/gpealat/coralreef/blob/main/Notebooks/1%20-%20EDA.ipynb) <br>
    This notebook provides an initial exploration of the dataset, including visualizations, statistical summaries, and handling missing data.
2. [Data cleaning](https://github.com/gpealat/coralreef/blob/main/Notebooks/2%20-%20Data%20cleaning.ipynb) <br>
    In this notebook, the dataset is cleaned by addressing missing values, handling duplicates, and preparing the data for machine learning models.
3. [Regression model](https://github.com/gpealat/coralreef/blob/main/Notebooks/3%20-%20Regression%20model.ipynb) <br>
    This notebook focuses on training regression models to predict the continuous Diversity Index.
4. [Classification model](https://github.com/gpealat/coralreef/blob/main/Notebooks/4%20-%20Classification.ipynb) <br>
    This notebook tests classification models by categorizing the Diversity Index into bins (e.g., low, medium, high) and predicting these classes.

## Conclusions

### Regression models
Given the dataset, we were not able to find a good balance to fit a regression model.
![alt text](https://github.com/gpealat/coralreef/blob/main/img/regression.png?raw=true)

We can see that Random Forest does a better job at fitting the data, but this is very relative and the quality of the results are not very good.

### Classification models
The classification models, however, showed a considerable improvement in performance for most of the models.

Although the problem initially seemed like a regression one, given the nature of our target feature, the results showed otherwise, which made us believe that the complexity of the data required another approach for its preparation or possibly the need for data acquisition, especially for the unbalance we have founded.

Finally, among the classification models we have tried, Random Forest was the one they showed the best results and, therefore, the ideal one for this problem and this dataset. 
![alt text](https://github.com/gpealat/coralreef/blob/main/img/f1s.png?raw=true)

