# DATA 201 -- Week 3 Assignment

## Visualization + Linear Regression (R → Python Bridge)

**Submission:** Jupyter Notebook (.ipynb)\
**Dataset:** housing.csv\
**Focus:** Interpretation \> Syntax

------------------------------------------------------------------------

# Part I -- Visualization (40 pts)

## A. Scatterplots and Aesthetics

1.  Create a scatterplot of **size vs price**.

    -   Label axes clearly.
    -   Add a meaningful title.

2.  Recreate the plot using `color = neighborhood` (use seaborn).

3.  Use transparency (`alpha`) to reduce overplotting.

### Short Answer (3--4 sentences)

-   What does seaborn automatically handle that matplotlib does not?
-   Why is transparency useful here?

------------------------------------------------------------------------

## B. Small Multiples (Faceting)

Create small multiples of **size vs price**, separated by `bedrooms`.

-   Keep scales consistent.
-   Add a clear overall title.

### Question

Does the relationship between size and price look similar across bedroom
counts?

------------------------------------------------------------------------

## C. Distribution and Categorical Plots

1.  Create a histogram of `price`.
2.  Create a density plot of `price`.
3.  Create a boxplot of `price` by `neighborhood`.

### Interpretation (short paragraph)

-   Do neighborhoods differ systematically in price?
-   What visual evidence supports your claim?

------------------------------------------------------------------------

# Part II -- Linear Regression for Inference (30 pts)

## A. Multiple Regression (R → Python)

In R, the model would be:

``` r
lm(price ~ size + bedrooms + neighborhood, data = df)
```

In Python:

1.  Fit the equivalent model using `statsmodels`.
2.  Report:
    -   Coefficient estimates
    -   Standard errors
    -   R²

------------------------------------------------------------------------

## B. Interpretation

Answer clearly:

1.  Interpret the coefficient on **size**, explicitly stating what is
    being held constant.
2.  Is size statistically significant? How do you know?
3.  What does R² tell us in this context?

------------------------------------------------------------------------

# Part III -- Prediction Workflow (20 pts)

Now switch goals: **Prediction instead of explanation**

1.  Split the data into training and test sets.
2.  Fit linear regression using `scikit-learn`.
3.  Compute:
    -   RMSE (on test set)
    -   R² (on test set)

------------------------------------------------------------------------

## Short Answer

-   Why does scikit-learn not report p-values?
-   Which workflow would you use for:
    -   Explanation?
    -   Prediction?
-   Why are these different goals?

------------------------------------------------------------------------

# Part IV -- Integrated Thinking (10 pts)

Create one polished figure that:

-   Shows size vs price
-   Colors by neighborhood
-   Includes a regression line
-   Has professional formatting

Then write 4--5 sentences:

-   Does the regression model match what you visually observed?
-   Did the visualization help you anticipate the model results?

------------------------------------------------------------------------

# Grading Rubric

  Component                      Points
  ------------------------------ ---------
  Visualization accuracy         20
  Visualization interpretation   20
  Regression implementation      20
  Regression interpretation      10
  Prediction workflow            20
  Integrated reasoning           10
  **Total**                      **100**
