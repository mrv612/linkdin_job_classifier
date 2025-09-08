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

# 2. Model

The model was created using Tensorflow and NLP methods learned during the course.

For a hyperparameter tuning process please refer to tuning-process-report.html, which is a sample of the entire parameter search. The complete report was over 400MB and will not be uploaded here.

The best model architecture found was:


. 8 hidden layers with 8 neurons each;

. batch_size=64;

. trained for 20 epochs;

. SGD opt.


Best model diagram, 86.85% accuracy in the test set.


<img width="1807" height="434" alt="image" src="https://github.com/user-attachments/assets/8dd4b3b6-446f-47c0-b0ac-cd8a6c9ef5e2" />


Tuning report of the best model

<img width="538" height="890" alt="image" src="https://github.com/user-attachments/assets/fc1895c1-b3f4-4ff6-8c5d-15fb76081008" />


#3. Webapp Streamlit

 
To see the model in action with Streamlit, use

$ git clone https://github.com/brunorosilva/nlp-classificacao-de-vagas.git
$ cd nlp-classificacao-de-vagas
~/nlp-classificacao-de-vagas $ pip install -r requirements.txt


and then

~/nlp-classificacao-de-vagas $ streamlit run dashboard.py


In the dashboard you'll be able to choose among simple examples, examples taken from LinkedIn which were not in the traning nor in the test set or even trying a manual input.

The webapp is extremely simple and it works as a POC, just choose among the options and the dashboard will create a bar plot showing the estimated probability among the three possible job titles.


<img width="1883" height="975" alt="image" src="https://github.com/user-attachments/assets/3e2bbd00-5e73-451b-8635-f94bae419049" />

# NLP - Classificação de Vagas


Este projeto é uma atividade da Especialização em Inteligência Artificial da PECE-Poli, disciplina de Processamento de Linguagem Natural.

O objetivo deste projeto é a criação de um modelo usando NLP capaz de receber uma descrição de vaga e retornar ao usuário qual é a visão do mercado sobre o título que este funcionário mais se adequa.


# Overview

