# King County Home Price Analysis

This repository offers an analysis of factors that influence housing prices in King County, WA

## This Repository

### Repository Directory

```
├── README.md        <-- Main README file explaining the project's business case,
│                        methodology, and findings
│
├── data             <-- Data in CSV format
│   ├── processed    <-- Processed (combined, cleaned) data used for modeling
│   └── raw          <-- Original (immutable) data dump
│
├── notebooks        <-- Jupyter Notebooks for exploration and presentation
│   ├── exploratory  <-- Unpolished exploratory data analysis (EDA) notebooks
│   └── report       <-- Polished final notebook(s)
│
├── references       <-- Data dictionaries, manuals, and project instructions
│
└── reports          <-- Generated analysis (including presentation.pdf)
    └── figures      <-- Generated graphics and figures to be used in reporting
```

### Quick Links

1. [Final Analysis Notebook](notebooks/exploratory/Second_Mission.ipynb)
2. [Presentation Slides](reports/presentation.pdf)
3. [Report Notebook](notebooks/reports/Report.ipynb)
### Setup Instructions

TODO: add setup instructions (e.g. the name of the Conda environment file)

## Business Understanding

A client in King County, WA wants to advise homeowners on home improvement projects that will add to the sale value of their homes.

## Data Understanding


## Data Preparation

I dropped all null values and 0's for every continuous variable. I also dropped low and high outliers for SqFtTotLiving and SalePrice.

## Modeling

I ended up using SqFtTotLiving, BldgGrade, Bedrooms and BathFullCount to try and predict SalePrice.

## Evaluation

I ended with being able to predict 44% of the variation, with violating the normality assumption due to the probability of the JB value is tiny. The homoscedasticity assumption was violated as well due to the check returning a value of 0. The model does not violate the linearity assumption and has very little multicollinearity.

## Conclusion

With my model I could predict that with every increase of building grade, the sale price would increase by about $3200. For every added bedroom the sale price would increase by about 3400. And for every added full bathroom the sale price would increase by about $3000.
Due to the model having a relatively low R-squared, large JB value and violating the homoscedasticity check, I would have to say I am not very confident in this model and it doesnt answer the business question very well.

Next steps would be to investigate the data more to see if there are features that would group the data cleaner in order to better predict.