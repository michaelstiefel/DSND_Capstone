# Predicting Customer Churn in Sparkify

This repository contains the jupyter notebooks for the Capstone Project of the Udacity
Data Scientist Nanodegree. Please check out this [medium blog post](https://medium.com/@ultimate_icterine_crab_125/predicting-customer-churn-with-aws-emr-and-pyspark-c7916219f53d) for a discussion
of this project and the results.

# Data

The data set is an artifical event log from a streaming service provided by Udacity. There is a mini data set (~100MB) and a full data set (~12GB) available in AWS S3 buckets (links in the jupyter notebooks).

# Files

There are two Jupyter Notebooks in this repository. The first DataScientist_Capstone.ipynb contains the full analysis conducted on the full data set on AWS EMR. The second dataset SparkifyVisualizations.ipynb contains the analysis on the mini dataset as well as visualizations in seaborn.

# How to run the jupyter notebook on the large dataset on AWS EMR

In order to run the jupyter notebook on the large dataset, I created a cluster on AWS EMR. Two hints were important for me. First, taking the latest release of AWS EMR, I could not connect the jupyter notebook to the cluster. Taking an earlier release 5.30.1, however, attaching the jupyter notebook to a cluster was not a problem. Depending on how many nodes you add to the cluster, the computation is still time-intensive. Therefore, in order to prevent timeouts, I found the following code [snippet](https://aws.amazon.com/premiumsupport/knowledge-center/emr-session-not-found-http-request-error/) useful to add to the setup when creating the cluster - it prevents timeouts when one cell takes too long to run.
