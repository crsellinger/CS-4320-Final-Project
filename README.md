# CS-4320-Final-Project

## Background
Hello and welcome to our project! This project aims to be a tool for developers to aide in their assessment of prospective of open-source software projects they wish to know more about. In particular, our project evaluates and gives the user useful data concerning the level of toxicity/negativity in the comments found within the Github working environment surrounding the project. We are able to gather this information from the Chaoss Augur development tool which assesses various stats about a projects health. Our project focusses on the sentiment score stat that is associated with messages in the Github respository which range from a -1 (Mostly Negative) message evaluation score to a +1 (Mostly Positive) message evaluation score. We use this score to provide the user with some helpful metrics in evaluating a repository the the community it fosters. Below are the metrics that are provided in this project which run via Jupyter Notebook pages and provide a visually pleasing graphical metric output.

### 1. ToxicMessagesPerUser.ipynb
Running this page will prompt the user to enter the name of a repository that exists within the reference Augur database that supplies the data that are project pulls from. After entering a valid database name, the Jupyter page will collect data about the sentiment scores of all messages made by each user in the repository. After the data has been tabulated, the user will be presented with a bar graph representation of the data with each bar giving the count of messages deemed toxic that were made by the bar's assigned user. Each graph will contain a maximum of 30 users and will also present a red line across the bar graph that shows the average toxic message count across that project.
Note: We used repository Loris for our testing, as it exists in the database and the count of contributers is low compared to others. This particular tabulation of data is a bit time consuming due to the nature of counting and accessing all of a contributor's messages across all contributors in the project.

### 2.ToxicMessageOverTime.ipynb
### 3.ToxicMessagesOverContribLifetime.ipynb
### 4.ToxicMessageCountByTotalMessageCountByUser.ipynb


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
