# K-Means-Clustering-Analysis

A1: PROPOSAL OF QUESTION:

"How can we segment customers into distinct groups based on continuous factors that influence churn?"


A2: DEFINED GOAL:

My goal is to identify different customer groups based on factors like monthly charges and bandwidth usage. I want to find out which of these factors are most related to customer churn. This will help us understand why customers churn and create better strategies to retain them.
 
B1: EXPLANATION OF THE CLUSTERING TECHNIQUE:

I chose k-means clustering because it helps me group customers based on continuous factors. The algorithm will find natural clusters in the data by grouping similar customers together. I expect to see distinct customer segments that share similar characteristics. This will help me understand which factors are linked to higher or lower chances of customers churning, giving me clear insights into what drives customer churn and how we can better target our efforts to retain them.

B2: SUMMARY OF THE TECHNIQUE ASSUMPTION:

One assumption of k-means clustering is that the data points can be grouped into distinct clusters with similar characteristics. This means that there are natural groupings in the data, where customers within each group are more similar to each other than to those in other groups. The algorithm assumes that the clusters are roughly spherical and of similar size, which helps in finding clear boundaries between different customer segments. This assumption allows me to effectively segment customers based on their continuous features and analyze patterns in customer churn.

B3: PACKAGES OR LIBRARIES LIST:

- Pandas: Helps me organize and manipulate the customer data.
- NumPy: Provides tools for numerical calculations and data handling.
- Scikit-learn: Offers the k-means clustering algorithm and related tools.
- Matplotlib: Used to create visualizations of the clustering results.
- Seaborn: Enhances data visualizations with attractive and informative statistical graphics.
 
C1: DATA PREPROCESSING:

The primary data preprocessing goal is to standardize the continuous variables, such as age, income, monthly charges, tenure, and bandwidth usage. Standardization ensures that all variables are on a similar scale, which is crucial for k-means clustering because the algorithm calculates distances between data points and centroids. Without standardization, variables with larger numerical ranges could disproportionately influence the clustering results, leading to biased clusters. By standardizing the data, we ensure that each variable contributes equally to the distance calculations, resulting in more accurate and meaningful customer segments.

C2: DATA SET VARIABLES:

- MonthlyCharge - Continuous
- Bandwidth_GB_Year – Continuous
  
I only focused on MonthlyCharge and Bandwidth_GB_Year so that I can draw insights from monthly charges and their usages per year.

C3: STEPS FOR ANALYSIS:

I first loaded the dataset and selected the two continuous variables I wanted to explore which was MonthlyCharge and bandwidth usage. Then, I checked for any missing values in these variables. Next, I standardized these variables so they would be on the same scale, which is important because I don't want any one factor to disproportionately influence the clustering results. Finally, I made sure the data was clean and formatted correctly for the k-means clustering analysis. This preparation helps me accurately identify distinct customer groups based on the continuous factors I'm analyzing.

D1: OUTPUT AND INTERMEDIATE CALCULATIONS:

Based on the Elbow Method plot and scatter plot matrix of clusters, the best number of clusters seems to be 4. We can see that at point 4 on the graph the line starts to flatten, showing us that adding more clusters doesn't significantly reduce the inertia or improve the model's fit. Using 4 clusters is a good balance, as it captures the main patterns in the data without making the model too complicated. This helps us understand the different customer groups effectively.


![image](https://github.com/user-attachments/assets/73dba497-63e9-4304-858b-1e342e7e2753)


![image](https://github.com/user-attachments/assets/cffcf578-e989-449a-a968-411ea0f07dba)

E1: QUALITY OF THE CLUSTERING TECHNIQUE:

The quality of the clusters created is quite good, with a Silhouette Score of 0.4878760152883964, indicating well-separated clusters. Each cluster shows distinct characteristics: Cluster 0 (Blue) has customers with low monthly charges and moderate bandwidth usage; Cluster 1 (Orange) includes those with moderate monthly charges and high bandwidth usage; Cluster 2 (Green) has customers with low monthly charges and low bandwidth usage; and Cluster 3 (Red) consists of customers with high monthly charges and moderate bandwidth usage. This clear differentiation helps us better understand customer groups and identify key factors related to churn.


E2: RESULTS AND IMPLICATIONS:

The clustering analysis revealed four distinct groups of customers, each with unique characteristics based on monthly charges and bandwidth usage. Cluster 0 (Blue) includes customers with low monthly charges and moderate bandwidth usage, indicating they may be more cost-sensitive. Cluster 1 (Orange) has customers with moderate monthly charges and high bandwidth usage, suggesting they are heavy internet users who might value high-speed or unlimited data plans. Cluster 2 (Green) consists of customers with low monthly charges and low bandwidth usage, likely representing a more basic usage group. Cluster 3 (Red) features customers with high monthly charges and moderate bandwidth usage, indicating a willingness to pay more for premium services. These insights allow us to create targeted strategies: offering budget plans for cost-sensitive customers in Cluster 0, enhancing high-speed data plans for heavy users in Cluster 1, providing basic but reliable services for Cluster 2, and maintaining premium service quality for Cluster 3. By understanding these specific needs and behaviors, we can customize our marketing and customer service efforts more effectively to improve satisfaction and reduce churn.


E3: LIMITATION:

One limitation of my analysis is that it didn't include important details like job or contract type. These details could also affect customer behavior and churn. So, we might be missing some important patterns that could help us understand our customers better. Including more types of data could give us a fuller picture.


E4: COURSE OF ACTION:

I recommend the company focus on targeted retention strategies. For clusters with a higher risk of churn, such as Cluster 0, offering special discounts or personalized service improvements could help retain these customers. For high-value customers in Cluster 3, introducing loyalty programs could increase satisfaction and encourage longer tenure. By customizing their approaches based on the specific needs and behaviors of each customer group, the company can reduce churn and improve customer satisfaction.




























