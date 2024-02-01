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
[Replication](#replication)  
[Contact](#contact-info)

# Background  

Nashville, TN is home to three primary professional sports teams - Nashville SC, the Predators, and the Titans. Nashville SC is relatively new compared to the other two franchises, which both have been in Nashville for over 25 years. Despite their youth, NSC has quickly developed a passionate fanbase. Now that they have had time to settle into the city, Nashville SC has turned its attention towards growing this fanbase. They want to understand Nashville sports fans. Who are they? Which teams do they actively support and why? What are some commonalities and differences between the fanbases? What do the fans think of the teams? We focus on the two latter questions. With this project, we hope to gain an understanding of Nashville sports fans' attitudes towards the three big teams - how they are the same, how they differ, and how they change based on various factors. We intend to avoid the biases associated with surveys, instead choosing to gather data from team-associated internet sources with the idea that the discussion that occurs there will be likely to contain fans' honest thoughts. Our data was pulled from Reddit and Instagram, although at this point, no analysis has been done on the Instagram data.

To process the data, we utilize a method called Aspect-Based Sentiment Analysis (ABSA), which is a two-step process. The first step takes in text and a list of aspects, returning the aspects from the list that are discussed in the text. The second step takes the same text, along with the output from the first step, and assigns a sentiment score to each aspect, representing how positive or negative the discussion around each aspect was in the text. For the Reddit data, the data was organized into threads, which contained a post and all comments on the post, and each thread received its own set of aspects and sentiment scores.

# Data

All data will be scraped from public sources. This includes data from Reddit posts from the following subreddits; r/NashvilleSC, r/TennesseeTitans, r/Predators, as well as official team Instagram accounts. Game data was retrieved from [Pro Football Reference](https://www.pro-football-reference.com/), [Football Reference](https://fbref.com/), [Hockey Reference](https://www.hockey-reference.com/). The collection of this data was free through the use of various API's.

# Models

OpenAI's gpt-3.5 is the model used in this project. This is a pre-trained model, thus requiring only FewShot prompting to be applied for this use case. Other models could be trained and tested on the data for further development.

# Repo Structure 

Give a description of how the repository is structured. Example structure description below:

The repo is structured as follows: Notebooks are grouped according to their series (e.g., 10, 20, 30, etc) which reflects the general task to be performed in those notebooks.  Start with the *0 notebook in the series and add other investigations relevant to the task in the series (e.g., `11-cleaned-scraped.ipynb`).  If your notebook is extremely long, make sure you've utilized nbdev reuse capabilities and consider whether you can divide the notebook into two notebooks.

All files which appear in the repo should be able to run, and not contain error or blank cell lines, even if they are relatively midway in development of the proposed task. All notebooks relating to the analysis should have a numerical prefix (e.g., 31-) followed by the exploration (e.g. 31-text-labeling). Any utility notebooks should not be numbered, but be named according to their purpose. All notebooks should have lowercase and hyphenated titles (e.g., 10-process-data not 10-Process-Data). All notebooks should adhere to literate programming practices (i.e., markdown writing to describe problems, assumptions, conclusions) and provide adequate although not superfluous code comments.

# Replication
See this section to replicate the data collection, cleaning, merging, and analysis. The following is a record of the order in which the notebooks were run to gather, clean, merge, and analyze the Reddit data (and other data needed for analysis). Note that some steps are interchangeable, but some notebooks require others to have been run as a prerequisite.

1. Gather the Reddit data: Reddit Notebooks/reddit_data_pull.ipynb
2. Run the ABSA
     * ABSA Notebooks/absa-NSC_full.ipynb
     * ABSA Notebooks/absa-Preds_full.ipynb
     * ABSA Notebooks/absa-Titans_full.ipynb
3. Clean the Games data: Clean Games Data.ipynb
     * Note: The raw games data was manually pulled (no code) from [Pro Football Reference](https://www.pro-football-reference.com/), [Football Reference](https://fbref.com/), and [Hockey Reference](https://www.hockey-reference.com/) and manually exported into .csv files.
4. Merge the Games data with the Reddit data: Merge Games Data.ipynb
5. Analyze the data: First Analysis.ipynb
     

# Contact Info

* Kit Connelly - cristian.c.connelly@vanderbilt.edu
* Sovann Chang - sovann.d.chang@vanderbilt.edu
