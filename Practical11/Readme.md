🌞 Sunspot Time Series Analysis
🧭 Purpose

This practical explores the long-term behaviour of solar activity by examining monthly average sunspot numbers. Using Python tools—including NumPy, pandas, Matplotlib, SciPy, and an MCMC framework—we visualize the data, fit probabilistic models, and estimate the parameters of a Gamma distribution across different subsets of the time series.

📊 Dataset Overview

Sunspots are cooler, magnetically active regions on the Sun’s surface. They tend to:

Occur in magnetically opposite pairs

Fluctuate in number according to an approximately 11-year solar cycle

The dataset analyzed here is the Monthly Mean Total Sunspot Number, containing:

Property	Description
Source	World Data Center responsible for the international sunspot number
Time span	January 1749 → November 2018
Frequency	Monthly
Variable	Average total sunspot count per month

This is a well-known dataset used frequently in solar physics and time-series research.

🧪 Workflow and Analysis Steps
🔹 Step 1 – Visualizing the Time Series

We begin by plotting the monthly sunspot index. Inspection of the figure reveals:

The overall evolution of solar activity

Repeating cycles roughly every 11 years

Changes in cycle amplitude from one period to the next

🔹 Step 2 – Fitting Gamma Models to Individual Cycles

To model the distribution of sunspot numbers, each 12-year segment of the data is treated as one cycle. For each segment we:

Fit a Gamma distribution

Estimate its shape (a) and scale/rate (b)

Compare the parameter values across cycles to see how the distribution’s form changes over time

This allows us to study how the magnitude and variability of solar activity evolve from cycle to cycle.

🔹 Step 3 – Empirical Distribution vs. Gamma Model

A histogram of the sunspot observations is produced and overlayed with the fitted Gamma density. This comparison provides:

Insight into how skewed the data are

A visual check of the Gamma model’s adequacy

An understanding of whether the distribution captures the tail behaviour and peak concentration

🔹 Step 4 – MNMC for Different Sample Windows

Using fixed parameters a = 4 and b = 10, we compute a Monte-Carlo–based estimate (MNMC) using:

The first 50 observations

All available observations

The last 50 observations

This highlights how estimates change depending on whether we look at early, full-length, or recent parts of the dataset. It also illustrates the effects of sample size and temporal location.

🔹 Step 5 – MCMC Diagnostics for a and b

MCMC sampling is used to obtain posterior distributions for the Gamma parameters. The analysis includes:

Discarding an initial burn-in period

Plotting trace graphs for a and b to check mixing and stability

Plotting histograms of the sampled parameter values

These diagnostics confirm whether the chains converge and whether the posterior estimates are reliable.

🔹 Step 6 – Predicting the Gamma Parameters

Finally, the posterior samples of a and b allow us to compute:

Point estimates (mean or median)

Credible intervals

Interpretations concerning distribution spread and tail behaviour

These results provide insight into:

How concentrated the sunspot distribution is

How often extreme high-activity months are expected

The overall uncertainty in the sunspot process’s underlying Gamma model

🧾 Summary

The monthly sunspot record offers a rich example of a long-term, cyclical time series. Through visualization, statistical modeling, and Bayesian inference, several key insights emerge:

The familiar ~11-year solar cycle appears clearly in the time-series plot.

A Gamma distribution is a fitting choice for modelling these non-negative, right-skewed observations.

Histogram comparisons demonstrate how well the Gamma model represents the empirical data.

MCMC sampling provides robust estimates for the Gamma parameters and quantifies their uncertainty.

MNMC analysis shows how parameter estimates behave when using early, full, and recent subsets of the data.

Trace plots verify chain convergence, supporting the reliability of the final parameter predictions.
