# linkdin_job_classifier



# NLP - Job Classification

This project is an activity of the Specialization in Artificial Intelligence at PECE-Poli, Natural Language Processing course.

The main objective of this project is to create a model using NLP which will be capable of receiving a job description and to predict what title this professional is most likely to be according to LinkedIn.


# Overview

The project was developed in three phases:

1. LinkedIn Data Scraping to create the dataset; 
2. Development of a Deep Learning model for multiclass classification;
3. Development of a web app using Streamlit in order to facilitate the interaction with the model.

# 1. Dataset

The dataset used to train the model was build using web scraping with Selenium, the scraping script is available in the scraper/scraper.py file.

The scraping process was to search for jobs with the titles of Data Scientist, Data Analyst and Data Engineer (a thousand of each), and to gatter the job description as given by the hiring company.

The dataset will not be available in this repo, due to the fact that no scraping authorization was made neither to LinkedIn nor to the individual companies.
