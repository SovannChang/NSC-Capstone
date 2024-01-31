# NSC-Capstone

This repository will serve as the codebase for the Nashville SC Marketing capstone project. This will be completed as the capstone project for Kit Connelly and Sovann Chang in the MSDS program at Vanderbilt University.

### Prerequisites
To most easily run this code out of the box, the following packages must be installed:

* pandas
* praw  
  NOTE: Need valid Reddit account, find instructions here: https://praw.readthedocs.io/en/stable/getting_started/quick_start.html  
  NOTE: Code currently uses account: kitconnelly. Please use own account for any additional data pulls.  
* datetime
* time
* os
* warnings
* openai  
  NOTE: Need an OpenAI Key, find instructions here: https://platform.openai.com/docs/quickstart?context=python  
* getpass
* re
* random
* cleantext
* langchain
* matplotlib
* scipy
* ast

# Quick navigation
[Background](#background)  
[Data](#data)  
[Models](#models)  
[Timeline](#timeline)  
[Repo Structure](#repo-structure)  
[Contact](#contact-info)

# Background  

Provide a broad overview of the purpose of the project.

# Data

All data will be scraped from public sources. This includes data from Reddit posts from the following subreddits; r/NashvilleSC, r/TennesseeTitans, r/Predators, game data from pro football reference, football ref, nhl ref?, and Instagram. The collection of this data was free through the use of various API's.

# Models

OpenAI's gpt-3.5 is the model used in this project. This is a pre-trained model, thus requiring only FewShot prompting to be applied for this use case. Other models could be trained and tested on the data for further development.

# Repo Structure 

Give a description of how the repository is structured. Example structure description below:

The repo is structured as follows: Notebooks are grouped according to their series (e.g., 10, 20, 30, etc) which reflects the general task to be performed in those notebooks.  Start with the *0 notebook in the series and add other investigations relevant to the task in the series (e.g., `11-cleaned-scraped.ipynb`).  If your notebook is extremely long, make sure you've utilized nbdev reuse capabilities and consider whether you can divide the notebook into two notebooks.

All files which appear in the repo should be able to run, and not contain error or blank cell lines, even if they are relatively midway in development of the proposed task. All notebooks relating to the analysis should have a numerical prefix (e.g., 31-) followed by the exploration (e.g. 31-text-labeling). Any utility notebooks should not be numbered, but be named according to their purpose. All notebooks should have lowercase and hyphenated titles (e.g., 10-process-data not 10-Process-Data). All notebooks should adhere to literate programming practices (i.e., markdown writing to describe problems, assumptions, conclusions) and provide adequate although not superfluous code comments.

# Contact Info

* Kit Connelly - cristian.c.connelly@vanderbilt.edu
* Sovann Chang - sovann.d.chang@vanderbilt.edu
