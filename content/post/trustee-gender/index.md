---
title: Classifying trustee gender using UK charity data
subtitle: Learn how to use Python and open charity data to predict a trustee's gender.

# Summary for listings and search engines
summary: Learn how to use Python and open charity data to predict a trustee's gender.

# Link this post with a project
projects: []

# Date published
date: '2023-09-15T00:00:00Z'

# Date updated
lastmod: '2023-09-15T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.

authors:
  - admin

tags:
  - Charity Data
  - Python
  - Trustees

categories:
  - Applied Data Analysis
---

## Overview

This is the first in a series of applied data analysis posts where I demonstrate some interesting analyses that can be done with open charity data and programming / statistical analysis.

For this analysis I focus on how you can classify the gender (or more accurately the sex) of a trustee and perform some simple analyses of gender diversity in the sector.

## Preliminaries

- Data on trustees was downloaded from the Charity Commission for England and Wales: [charity_trustee](https://register-of-charities.charitycommission.gov.uk/register/full-register-download)
- Data on the field of activity / "industrial" sector for charities was downloaded from the Charity Classification project: [UKCAT](https://github.com/charity-classification/ukcat) 

## Classifying trustee gender

I used the `gender-guesser` package in Python to classify (predict) the gender of a trustee using their first name. This step was restricted to individuals (perhaps an obvious point but some trustees of charities are actually organisations e.g., NHS trusts act as trustees of health charities). The programming code can be found [here]() but for now I'll comment on some of the limitations:
1. Some individuals do not provide a first name e.g., Lt M. R. Smith. We could make some assumptions to generate further classifications e.g., most lieutenants are male.
2. Some names are not recognised by the classifier - these mainly seem to be South Asian or African in origin, therefore there is a risk the classifier is biased towards English-origin first names.
3. The first names need to be in *title* case e.g., Fiona, not fiona | FIONA

The results of the classification for the 913,975 trustee names:
| Gender | Count |
|--------|-------|
| male   | 439,261 |
| female   | 378,973 |
| unknown  | 45,391 |
| mostly_female | 26,658 |
| mostly_male | 15,620 |
| androgynous | 8,072 |

## Analysing gender diversity

We can now aggregate the trustee data to charity level i.e., summarise the number of trustees in each of these categories for each charity. The trustee data seem to refer to c. 140,000 currently registered charities. We can then merge data on a charity's field of activity (e.g., Culture and recreation) and its geographic location (e.g., local authority) to explore patterns in gender diversity. This analysis was conducted in Stata but easily have been done in Python, R etc.

We restrict our analysis to individuals classified as *male* or *female* though it would be interesting to examine patterns in the distribution of the unclassified (*unknown*) trustees.

### Gender diversity by field of activity



### Gender diversity by geographic area

## License

Copyright 2023-present [Diarmuid McDonnell](https://diarmuidmcdonnell.com).