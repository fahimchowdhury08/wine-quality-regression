# Project Proposal: Predicting Wine Quality from Physicochemical Properties

## Research Question

Can we predict a red wine's sensory quality score (rated 0–10) using only its
measurable physicochemical properties (acidity, sugar, sulfur dioxide levels,
density, pH, sulphates, alcohol content)? Which of these properties are the
strongest predictors of quality, and how accurately can a regression model
estimate quality without human tasting?

## Dataset

- **Name:** Wine Quality Data Set (red wine subset)
- **Source:** UCI Machine Learning Repository
- **Link:** https://archive.ics.uci.edu/dataset/186/wine+quality
- **Original creators:** Cortez, P., Cerdeira, A., Almeida, F., Matos, T., & Reis, J. (2009)
- **Size:** 1,599 samples, 11 physicochemical input features, 1 output (quality score)
- **License:** CC BY 4.0

The data comes from physicochemical lab tests on samples of the Portuguese
"Vinho Verde" red wine, paired with a quality score derived from sensory
evaluation by wine experts. No data on grape variety, brand, or price is
included, only lab-measured chemistry and the resulting quality rating.

## Related Work (Literature Scan)

**1. Original dataset paper — Cortez et al. (2009).**
The team that created this dataset originally modeled wine quality using
data mining techniques (including regression) applied to the same
physicochemical measurements used here, establishing that quality can be
estimated reasonably well from chemistry alone, though the sensory scores
are subjective and imbalanced (far more "average" wines than excellent or
poor ones), which limits accuracy at the extremes.

**2. Dahal, K. R., Dahal, J. N., Banjade, H., & Gaire, S. (2021). "Prediction
of Wine Quality Using Machine Learning Algorithms." Open Journal of
Statistics, 11(2), 278–289.**
This study compared several regression and machine learning approaches
(including linear regression, ridge/lasso, and ensemble methods) on the same
UCI wine quality data, finding that ensemble and non-linear models tend to
outperform simple linear regression, and that alcohol content and volatile
acidity are consistently among the most important predictors of quality.

## Planned Approach

1. Exploratory data analysis: distributions, correlations, and class balance
   of the quality score.
2. Baseline linear regression on the 11 physicochemical features.
3. Compare against regularized regression (Ridge/Lasso) to address
   multicollinearity between features.
4. Evaluate with RMSE and R², informed by how prior work handled the
   imbalance in quality scores.
