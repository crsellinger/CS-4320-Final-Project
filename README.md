# CS-4320-Final-Project

## Background
Hello and welcome to our project! This project aims to be a tool for developers to aide in their assessment of prospective open-source software projects they wish to know more about. In particular, our project evaluates and gives the user useful data concerning the level of toxicity/negativity in the comments found within the Github working environment surrounding the project. We are able to gather this information from the Chaoss Augur development tool which assesses various stats about a projects health. Our project focuses on the sentiment score stat that is associated with messages in the Github respository which range from a -1 (Mostly Negative) message evaluation score to a +1 (Mostly Positive) message evaluation score. We use this score to provide the user with some helpful metrics in evaluating a repository and the community it fosters. Below are the metrics that are provided in this project which run via Jupyter Notebook pages and provide a visually pleasing graphical metric output.

Note: We used repository Loris and contributor ID 389737 for our testing, as it exists in the database and the count of contributers is low compared to others. This particular tabulation of data is a bit time consuming due to the nature of counting and accessing all of a contributor's messages across all contributors in the project.

### 1. ToxicMessagesPerUser.ipynb
Running this page will prompt the user to enter the name of a repository that exists within the reference Augur database that supplies the data that are project pulls from. After entering a valid database name, the Jupyter page will collect data about the sentiment scores of all messages made by each user in the repository. After the data has been tabulated, the user will be presented with a bar graph representation of the data with each bar giving the count of messages deemed toxic that were made by the bar's assigned user. Each graph will contain a maximum of 30 users and will also present a red line across the bar graph that shows the average toxic message count across that project.


### 2.ToxicMessageOverTime.ipynb
This metric will show the number of toxic messages per month of a given repository. Prompts user to enter the name of a repository that exists within the reference Augur database. After entering a valid database name, the Jupyter page will collect the average sentiment scores for every message in the history of the repo and orders them by month. It then gathers all the possible months to be used for calculating. The user will be presented with a line graph(s) of the percentage of toxic messages per month over the repository's lifetime. Each graph will contain a max of 30 months.

### 3.ToxicMessagesOverContribLifetime.ipynb
This metric will show the number of toxic messages per month for a given user within a given repository. Prompts user to enter the name of a repository that exists within the reference Augur database and a specific contributer within the working repository. After entering a valid database name and contributor ID, the Jupyter page will gather the average sentiment scores for every message over the lifetime of the repository and order them by month. The user will be presented with a line graph of the contributor's number of toxic messages per month within the given repository. Each graph will contain a max of 30 months.

### 4.ToxicMessageCountByTotalMessageCountByUser.ipynb
This metric will show the number of toxic messages per month for a given user against their total number of messages per month. Prompts user to enter a contributor ID that exists within the reference Augur database. After entering a valid contributor ID, the Jupyter page will collect the average sentiment scores, orders them by month, and calculates the total number of messages and number of toxic messages. The user will be presented with a double bar graph, the blue bar representing the toxic messages and the green bar representing the total messages for each month. Each graph will contain a max of 30 months.

## Prerequisites and Setup:
Our project utilizes Jupyter Notebooks and shares its a lot of it's structure with Chaoss's Augur Community Reports project and repository. The prerquisits and setup will closely mirror that project. That projects steps and processes will be copied here, but can also be referenced [here](https://github.com/chaoss/augur-community-reports "Augur Community Reports"). If you wish to develop your own Jupyter Notebook pages, reference that page.


### Prerequisites
1. Python 3.x
2. pip
3. virtualenv package `pip3 install virtualenv` 

### Setup augur-community-reports
1. Fork this repository
2. Clone your fork of the repository locally
```
git clone https://github.com/<your-fork>/CS-4320-Final-Project
````
3. Create your python virtual environment wherever you routinely store them. We use a `virtualenvs` directory. 
```
virtualenv --python=python3 virtualenvs/augur-toxicity-reports
```
4. Navigate to the toxicity-reports directory
```
cd CS-4320-Final-Project/toxicity-reports
```
5. Activate your virtual environment
```
source  ../../virtualenvs/augur-toxicity-reports/bin/activate
```
6. Navigate to the RequirementsFiles directory
```
cd ../RequirementsFiles
```
7. Install the necessary Python libraries for Python 3.8 and earlier
```
pip install -r requirements.txt
```
8. Install the necessary Python libraries for Python 3.9 and later
```
pip install -r requirements3.9.txt 
```
9. Go back to the toxicity-reports directory
```
cd ../augur-toxicity-reports
```
10. Run Jupyter Lab
```
jupyter lab
```
11. In the Jupyter Lab terminal you can now select and run any of the pages/metrics we have provided. We hope you enjoy your time using our Augur Toxicity Reports tool
