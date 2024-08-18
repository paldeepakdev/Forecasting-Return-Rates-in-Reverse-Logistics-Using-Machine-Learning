# Large Retailer Customer Transaction Analysis

This repository contains a comprehensive analysis of customer transactions from a large retailer. The analysis covers data preprocessing, univariate and bivariate analysis, and feature engineering. The aim is to uncover insights and trends in customer purchase behavior, product returns, and other relevant metrics.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset Description](#dataset-description)
- [Installation](#installation)
- [Usage](#usage)
  - [Data Preprocessing](#data-preprocessing)
  - [Univariate Analysis](#univariate-analysis)
  - [Bivariate Analysis](#bivariate-analysis)
  - [Feature Engineering](#feature-engineering)
- [Results](#results)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The goal of this project is to analyze customer transaction data from a large retailer to gain insights into customer behavior, product categories, and the factors influencing product returns. The analysis also involves data cleaning, visualization, and feature engineering to prepare the dataset for further machine learning tasks, such as predicting product returns.

## Dataset Description

The dataset contains transaction data with the following features:

- **Transaction ID**: Unique identifier for each transaction.
- **Month Code**: Coded month of the transaction.
- **Product Category Code**: Coded product category.
- **Product Subcategory Code**: Coded product subcategory.
- **Quantity**: Number of items purchased.
- **Rate**: Price per item.
- **Amount**: Total transaction amount.
- **Tax**: Tax amount applied to the transaction.
- **Delivery Charges**: Delivery charges applied to the transaction.
- **Payment Mode**: Mode of payment used in the transaction.
- **Store Type**: Type of store where the purchase was made.
- **Reviews**: Customer reviews rating.
- **Customer ID**: Unique identifier for each customer.
- **Income**: Annual income of the customer.
- **City Code**: Coded city where the transaction occurred.
- **Return**: Indicates whether the product was returned.
- **Date of Birth**: Customer's date of birth.
- **Gender**: Customer's gender.
- **Marital Status**: Customer's marital status.
- **Education Code**: Coded educational level of the customer.
- **Profession Code**: Coded profession of the customer.

## Installation

To run this project locally, follow these steps:

1. Clone this repository:
    ```bash
    git clone https://github.com/your-username/large-retailer-analysis.git
    ```

2. Navigate to the project directory:
    ```bash
    cd large-retailer-analysis
    ```

3. Create a virtual environment and activate it:
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

4. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

The project is organized in a single Jupyter Notebook that walks through the entire analysis. Below is a brief overview of the major steps involved.

### Data Preprocessing

1. **Data Loading**:
    - The dataset is loaded using `pandas`.
    - NaN values in the `Delivery Charges` column are filled with 0.
    - Certain columns are dropped, such as `Transaction ID`, `Customer ID`, and `DOB` as they are not needed for the analysis.
  
2. **Mapping Categorical Codes**:
    - Categorical codes like `Month Code`, `Product Category Code`, etc., are mapped to human-readable names using dictionaries.

3. **Handling Missing Values**:
    - Missing values in columns `Reviews` and `Income` are dropped to ensure clean data.

### Univariate Analysis

- **Category-wise Distribution**:
  - Visualizations like bar charts and histograms are used to explore the distribution of various categorical and numerical variables.
  
- **Distribution of Numeric Features**:
  - Histograms are used to explore the distribution of numeric features like `Rate`, `Tax`, and `Amount`.

### Bivariate Analysis

- **Relationship Between Variables**:
  - Count plots and box plots are used to examine relationships between different variables, such as `Rate` and `Return`, `Amount` and `Return`, and others.
  - Pair plots are used to explore relationships between multiple numeric variables like `Rate`, `Amount`, `Tax`, `Delivery Charges`, and `Income`.

### Feature Engineering

- **Encoding Categorical Variables**:
  - Categorical variables are converted into dummy/indicator variables using `pd.get_dummies()`.
  - The final dataset consists of the original numeric variables along with the newly created dummy variables.

## Results

The analysis provides insights into:

- **Customer Purchase Behavior**: Popular product categories, common payment modes, and store types.
- **Product Returns**: Which products are more likely to be returned, and how factors like `Rate` and `Amount` influence returns.
- **Income Distribution**: How income varies among different customer segments and its relationship with purchasing behavior.

## Future Work

The next steps for this project could include:

- **Machine Learning Modeling**: Using the prepared dataset to build predictive models for forecasting product returns or customer churn.
- **Advanced Feature Engineering**: Creating more sophisticated features based on the existing ones to improve model performance.
- **Segmentation Analysis**: Performing clustering to segment customers based on purchasing behavior and demographics.

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request with your proposed changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
