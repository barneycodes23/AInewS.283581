# Artificial Intelligence and Machine Learning Project

### Dataset Used: ShopEasy

#### Group Members:
* Martina Fagnani - 
* Banuka Kottage Don - 287711
* Matilde Tambini - 286431

# Introduction

Our goal in this project is to identify the diverse user base and strategically segment the users with the aim of providing a personalized user experiences and special promotions which meets the unique preferences of the customers in each of the different segments that would ultimately lead to a satisfied and a personalized shopping experience of their users.

# Methods

In order to access the jupyter notebook file we need to create an enviornment for it. Follow the following steps in order to create the notebook:

- Save the file named "enviornment.yml", which is uploated in the repository.
- Open the terminal or Command Prompt and run the following code:
  - (RUN): conda env create -f environment.yml
- In order to activate this enviornment run the following code:
  - (RUN): conda activate aiproject_env
- Finally **Run** the jupyter notebook.

The aim of this analysis is identifing indistinguishable segments from the data provided in the shopEasy.csv and presenting the acknowledged patterns ---. The outline of this process is illustrated with the aid of a flowchart.




# Experimental Design

Initially, we conducted an assesment to identify the presence of any duplicated rows with the dataset as duplicated rows would have a significant impact with the interpretation of the graphical representaions. After learning about the absence of duplicated rows in our dataset we proceeded to the subsequent step, which was an assesment to identify the presence of **null values** within the dataset which ensures the completeness and integrity of the dataset and addresses any potential gaps or omissions in the final results. The sole purpose of the column "personId" was to check if there are redundent rows in the dataset, after our analysis we deemed that no duplicated rows existed within the dataset and therefore the purpose of the column "personId" was served therefore the decision was made to remove this column from the dataset. 

We further analyzed the dataset and identified columns that were deemed vague and irrelevant to our analysis which did not align with final aim of this project. We also examined the dataset to identify columns exhibiting perfect correlation, indicating that these columns do not need to be presented individually. Following this assessment, we proceeded to eliminate these identified columns from the dataset ensuring a streamlined and optimized structure for further analysis.

We discovered the presence of **categorical variables**. Given the distinction between categorical and continuous variables, our approach involved treating these two types of variables differently. Addressing the catergorical varialbles we decided to encode these variables which enables us to facilitate comparisons later in the project. Through visualizing categorical variables with filters, we were able to discern clear results, such as identifying the city with the highest number of customers and which city has the customers who spends the most. We gained insights into the customer bases as well. For instance, we observed a higher number of customers are students in Chicago compared to the other cities.


