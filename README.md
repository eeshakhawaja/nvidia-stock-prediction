# NVIDIA Stock Analysis and Next-Day Price Prediction

## Overview

I built this project to explore whether historical stock data can be used to predict the next day’s price movement for NVIDIA shares.

The main goal was not just to train a model, but to understand what can realistically be learned from financial data, how useful certain features are, and where machine learning starts to struggle in a noisy real-world setting like the stock market.

---

## What this project covers

In this project, I:

* cleaned and prepared historical NVIDIA stock data
* explored trends and short-term price behaviour
* created new features such as day of the week and moving averages
* built a Decision Tree model to classify next-day price direction
* evaluated the model and reflected on its limitations

---

## Dataset

The dataset includes historical NVIDIA stock information such as:

* Date
* Price
* Open
* High
* Low
* Volume
* Daily percentage change

---

## My approach

### 1. Data cleaning

I first cleaned the raw dataset by:

* converting the date column into datetime format
* converting volume values into numeric form
* removing percentage symbols and converting change values into floats
* sorting the data in chronological order

This was important because the raw data was not immediately ready for analysis or modelling.

### 2. Exploratory analysis

Before modelling, I spent time understanding the data itself.

I looked at:

* the distribution of daily percentage change
* general price behaviour over time
* whether certain days of the week seemed to be linked to upward or downward movement
* whether being below the 20-day moving average had any relationship with the next day’s direction

This part of the project helped me think more carefully about what features might actually be useful.

### 3. Feature engineering

To make the problem more suitable for machine learning, I created variables such as:

* **Day of the Week**
* **20-Day Moving Average**
* **Target_Direction**, which captures whether the next day’s closing price increased or decreased

### 4. Modelling

I approached the task as a **classification problem** rather than trying to predict the exact next-day price.

I used a **Decision Tree** model because it is interpretable and useful for understanding how feature-based decisions are being made.

### 5. Evaluation

I evaluated the model using standard classification metrics and compared performance in the context of financial prediction, where even seemingly decent results need to be interpreted carefully.

---

## What I found

A few things stood out from this project:

* short-term stock prediction is much harder than it first appears
* financial data is noisy, and patterns are often weak or unstable
* feature engineering mattered more than simply choosing a model
* some patterns appeared in the exploratory analysis, but they were not strong enough to make prediction easy

This made the project useful not just as a machine learning exercise, but as a lesson in how important it is to question model performance in real-world settings.

---

## Limitations

This project only uses historical price-based features, so it does not account for things like:

* news and market sentiment
* macroeconomic events
* earnings releases
* broader sector behaviour

That means the model is working with only part of the picture.

It is also important to note that stock market data can be especially prone to overfitting, so good performance on one split does not necessarily mean the model would generalise well in practice.

---

## Tools used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Final thoughts

What I liked most about this project was that it pushed me to think beyond “build a model and report accuracy.”

It made me think more seriously about:

* how to structure a prediction problem
* how to create useful features
* how to interpret results carefully
* and how to be honest about the limits of machine learning

Even though the project focuses on NVIDIA stock data, the broader value for me was learning how to approach noisy data in a structured way.
