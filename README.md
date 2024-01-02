# Artificial Intelligence and Machine Learning Project

### Dataset Used: ShopEasy

#### Group Members:
* Martina Fagnani - 283581
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

The aim of this analysis is to identify indistinguishable segments from the data provided in the shopEasy.csv and acknowledge the patterns for tailoring marketing and special promotions to each of the identified segments. We initiate the process by preprocessing the dataset, following this, we encode categorical variables and visualize the dataset. Given the nature of the task is a clustering problem, we choose to employ K-means and hierarchical structuring as our models for the segmentation process. To measure the performance of our algorithms with the dataset, we utilize relevent metrics.

# Experimental Design

Initially, we conducted an assesment to identify the presence of any duplicated rows with the dataset as duplicated rows would have a significant impact with the interpretation of the graphical representaions. After learning about the absence of duplicated rows in our dataset we proceeded to the subsequent step, which was an assesment to identify the presence of **null values** within the dataset which ensures the completeness and integrity of the dataset and addresses any potential gaps or omissions in the final results. The sole purpose of the column "personId" was to check if there are redundent rows in the dataset, after our analysis we deemed that no duplicated rows existed within the dataset and therefore the purpose of the column "personId" was served therefore the decision was made to remove this column from the dataset. 

We further analyzed the dataset and identified columns that were deemed vague and irrelevant to our analysis which did not align with final aim of this project. We also examined the dataset to identify columns exhibiting perfect correlation, indicating that these columns do not need to be presented individually. Following this assessment, we proceeded to eliminate these identified columns from the dataset ensuring a streamlined and optimized structure for further analysis.

We discovered the presence of **categorical variables**. Given the distinction between categorical and continuous variables, our approach involved treating these two types of variables differently. Addressing the catergorical varialbles we decided to encode these variables which enables us to facilitate comparisons later in the project. Through visualizing categorical variables with filters, we were able to discern clear results, such as identifying the city with the highest number of customers and which city has the customers who spends the most. We gained insights into the customer bases as well. For instance, we observed a higher number of customers are students in Chicago compared to the other cities.

We introduced a new variable, "composite_score", by combining the frequency index and account total. This composite_score serves as a benchmark value against which we can compare the performance of other coloumns. Then we generate a correlations heatmap to enhance our understanding of the relationships and to visualize the correlations within the dataset. We also deemed that a value with a correlation less that 0.01 comapred to composite_score would be deemed insignificant for further analysis hence we removed those coloumns.

# Results

The initial observation from the bar chart indicates a nearly equal distribution of customers across the three different cities. Additionally, the chart reveals a similarity in the usage of account types among customers in these three locations. This suggests a consistent pattern in customer distribution and account preferences across the cities. Following this we introduced various filters to discern distinctions, a notable finding emerged when visualizing the distribution of high spenders across the three cities. It becomes evident that Location 2 (Los Angeles) exhibits the highest number of high spenders. Several factors could contribute to this trend, with a primary consideration being the **effectiveness of marketing and branding efforts**. It is plausible that our initiatives resonated more successfully in the city with a higher concentration of customers who exhibit greater spending tendencies. As a strategic response, there is an opportunity to **channel marketing and branding efforts more intensively in the other two cities** to potentially enhance customer engagement and spending.

Upon analyzing the monthly payments made by high spenders, a distinct variation in the **number of student accounts** becomes evident, particularly between New York (NY) and Chicago. Notably, Location 2 (LA) **does not** exhibit a substantial number of student accounts in comparison. This divergence suggests a unique demographic composition, with a **higher concentration of student accounts** using this feature is **observed in New York and Chicago**.Further analysing of this demographic distinction may inform targeted strategies for student engagement and tailored marketing efforts in these specific locations.

Upon analyzing the data using the frequency index, we observed that all three locations and the various account types exhibit **relatively similar shopping patterns and frequencies**. This parallelism in shopping behavior suggests a **consistency in customer engagement and transactional activities across the different locations and account categories**. 

We used both K-means and hierarchical clustering techniques to segment the dataset, categorizing it into seven distinct clusters based on various essential metrics such as account total, frequency index, item costs, item buy frequency, and more. This clustering methodology provides a sophisticated comprehension of customer diversity, facilitating the formulation of precise strategies for marketing and engagement. Subsequently, we will explore the specific characteristics associated with each cluster in detail:
- Cluster 0 :
  - Moderate account totals.
  - Relatively lower item costs.
  - Consistent yet restrained purchase frequency.
  
   <p align="left">
  <img src="https://github.com/barneycodes23/AInewS/blob/main/images/c0.png" width="200">
</p>

- Cluster 1:
  - Affluent customer segment.
  - Higher account totals.
  - Elevated item costs.
  - Near-maximum item buy frequency, signifying an active and prosperous user base.
  <p align="left">
  <img src="https://github.com/barneycodes23/AInewS/blob/main/images/c1.png" width="200">
</p>

- Cluster 2:
  - Moderate account totals.
  - Lower item costs.
  - Somewhat reduced frequency of purchases.
  <p align="left">
  <img src="https://github.com/barneycodes23/AInewS/blob/main/images/c2.png" width="200">
</p>

- Cluster 3:
  - Diverse customer base.
  - High account totals.
  - Variable item costs.
  - Varied purchase frequencies.
  <p align="left">
  <img src="https://github.com/barneycodes23/AInewS/blob/main/images/c3.png" width="200">
</p>

- Cluster 4:
  - Moderate account totals.
  - Diverse item costs.
  - Moderate purchase frequency.
    <p align="left">
  <img src="https://github.com/barneycodes23/AInewS/blob/main/images/c4.png" width="200">
</p>

- Cluster 5:
  - Smaller group of high-value customers.
  - Significantly higher item costs.
  - Consistent, near-maximum item buy frequency.
    <p align="left">
  <img src="https://github.com/barneycodes23/AInewS/blob/main/images/c5.png" width="200">
</p>

- Cluster 6:
  - Moderate account totals.
  - Moderate item costs.
  - Notably high item buy frequency.
    <p align="left">
  <img src="https://github.com/barneycodes23/AInewS/blob/main/images/c6.png" width="200">
</p>

We utilized the silhouette score as a performance metric to evaluate the clustering algorithms, and the results indicated that K-means performed optimally with our dataset, achieving a silhouette score of 0.22, we have decided to adopt this approach for the customer segmentation.

![Alt Text](https://github.com/barneycodes23/AInewS/blob/main/images/kmeans.png)

# Conclusion

In conclusion, it is important to understand that the observed outcome of not achieving a high silhouette score, typically considered to be above 0.8, is **entirely anticipated**. This expectation arises from the nature of grouping a substantial dataset with a relatively limited number of columns(5-6). Furthermore, the **constrained range within our columns**, exemplified by the presence of only three account types, contributes to this anticipated outcome. Another factor to consider is that we are primarily dealing with categorical variables, which can pose challenges in achieving high silhouette scores in clustering analyses. 

Considering all the factors discussed, achieving a silhouette score of 0.22 is indeed commendable. It signifies that, despite the complexities inherent in the dataset, the clustering algorithms, particularly K-means, have successfully identified discernible patterns and segments. This outcome provides a valuable foundation for targeted marketing and engagement strategies tailored to each cluster, thus optimizing the efficiency and ensuring that they are personalized to the specific characteristics and preferences within each identified cluster. This level of personalization enhances the potential impact of marketing and engagement efforts, nurturing a meaningful connection with the diverse customer base represented by the distinct clusters.

