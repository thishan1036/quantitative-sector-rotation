{\rtf1\ansi\ansicpg1252\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww14580\viewh19980\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Quantitative Sector Rotation Strategy\
\
## Project Objective\
This project develops and backtests a machine learning model to rotate monthly between 11 US sector ETFs. The primary objective was to determine if a data-driven, active rotation strategy could consistently outperform a passive S&P 500 (SPY) benchmark. The entire workflow, from data acquisition and feature engineering to walk-forward validation with an expanding window and performance analysis, is contained within the notebook.\
\
## Key Findings & Conclusion\
* **Model Failure Analysis:** The primary models (Random Forest, Elastic Net) failed to provide a reliable predictive edge for selecting top-performing sectors. The investigation into this failure revealed two key insights into model behavior:\
    * **1. Environmental Bias:** The Elastic Net model became "lazy," learning to simply predict positive returns after being trained on a dataset composed of an 82% bull market regime. This resulted in a high directional accuracy that was mimicking the broader market and ultimately meaningless.\
    * **2. Feature Obsession:** The Random Forest model became over-reliant on the highly volatile momentum features of a single sector (XLE - Energy), failing to create a generalized, all-sector model.\
* **Conclusion:** This project is a case study in the critical importance of robust backtesting and model diagnostics. It demonstrates that a superficially positive result can be misleading without a deep analysis of the biases a model learns from its training data.\
\
## Technology Stack & Methods\
* **Languages/Libraries:** Python, Pandas, NumPy, Scikit-Learn, Matplotlib, `yfinance`, `pandas_datareader`\
* **Techniques:** Time-Series Analysis, Feature Engineering, Walk-Forward Validation, Random Forest, Elastic Net, Model Diagnostics\
\
## Project Structure\
* **`.ipynb Notebook`**: The main file containing the entire analysis, from data downloading and cleaning to modeling, backtesting, and conclusion.\
* **`.gitignore`**: Specifies files and directories to be ignored by Git.\
\
## How to Run\
1.  Clone the repository to your local machine.\
2.  Ensure you have the required libraries from the Technology Stack installed.\
3.  Run the `sector_rotation.ipynb` notebook. The script is self-contained and downloads all necessary market data via APIs.}