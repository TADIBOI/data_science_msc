Bivariate & Multivariate Analysis
Dataset: Use the same dataset you used previously in class/notebook.

Submission: One Jupyter Notebook (.ipynb) with code, plots, and short written answers (1–2 sentences each).

Tools: Python + pandas + numpy + matplotlib (and optional scikit-learn for scaling/imputation).

Learning Goals
Perform bivariate analysis using covariance and correlation (Pearson and Spearman).
Perform multivariate analysis using covariance/correlation matrices and visual summaries.
Create appropriate, readable visualizations that support interpretation (not just plots for the sake of plotting).
Recognize issues like outliers, nonlinearity, and scale differences.
Constraints
Your notebook should be understandable by someone else: clear headings + minimal but useful commentary.
Every visualization must have: title, axis labels, and (when relevant) a legend.
Part A : Quick Data Audit
Load the dataset.
Print:
shape (#rows, #columns)
column names + data types
missing values count per column
basic descriptive stats for numeric columns (describe())
Write 2–3 sentences: Which columns look like potential targets (outcomes) and which look like predictors (inputs)?
Part B : Bivariate Analysis
Pick two pairs of variables for bivariate analysis:
Pair 1: two numeric variables where you expect a relationship.
Pair 2: two numeric variables where you are not sure (or suspect weak/nonlinear/outlier-driven effects).

B1. Visualize relationships (must include at least 3 visuals)
Scatter plot for Pair 1 (include a trend line if you know how, optional).
Scatter plot for Pair 2.
One additional plot that helps interpretation (choose one):
scatter plot with points colored by a third variable (if applicable), or
boxplot/violin comparing a numeric variable across categories (if you have a categorical column).
B2. Quantify: covariance, Pearson, Spearman
Compute the covariance for Pair 1 and Pair 2.
Compute Pearson correlation (r) for Pair 1 and Pair 2.
Compute Spearman rank correlation for Pair 1 and Pair 2.
For Pair 1, compute and report r² and explain in 1–2 sentences what it means in context.
B3. Outlier / Nonlinearity check
For one of your pairs, identify potential outliers (e.g., top/bottom 1% by one variable or using IQR rule).
Recompute Pearson correlation with and without the outliers.
Write 2–3 sentences: Did the correlation meaningfully change? What does that imply?
Part C: Multivariate Analysis
C1. Correlation matrix (numeric features)
Select all numeric columns (or a relevant subset if there are too many).
Create a correlation matrix (Pearson) and display it as a heatmap or well-formatted table.
Identify:
the top 3 strongest positive correlations (excluding self-correlation), and
the top 3 strongest negative correlations.
Write 2–3 sentences: Which relationships might indicate redundancy (multicollinearity risk)?
C2. Scaling / normalization impact
Pick 3 numeric features that have noticeably different scales (e.g., one large-range and one small-range).
Standardize them (z-score) and show:
a table of before vs after summary stats (mean, std, min, max), and
one visualization comparing distributions before vs after (e.g., histograms or boxplots).
Write 2 sentences: Why is scaling important for some multivariate methods (give one example method)?
C3. Missing values (brief but concrete)
Choose one column with missing values (if none exist, simulate by setting ~5% of entries in one numeric column to missing).
Try two approaches:
Drop missing rows for that subset, and
Impute missing values (mean or median for numeric).
For one bivariate pair that involves that column, compare a key statistic (Pearson r or covariance) under both approaches.
Write 2 sentences: Which approach seems more stable and why?
Required Deliverables
A well-structured notebook with headings: Part A, Part B, Part C.
At least 4 visualizations total (minimum: 2 scatterplots + 1 additional for bivariate + 1 heatmap/distribution plot).
All requested statistics: covariance, Pearson r, Spearman, r², correlation matrix, and the outlier comparison.
Short written interpretations (1–3 sentences each) for each part.
Optional (if time remains)
Compute a partial correlation (relationship between X and Y controlling for Z) and compare to Pearson r.
Create a pairplot-like mini-dashboard (a few scatterplots for the top correlated variables) and summarize patterns.