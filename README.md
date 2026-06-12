# Bank Customer Churn Prediction & Analytics

<img width="6150" height="3525" alt="Bank Customer Churn_page-0001" src="https://github.com/user-attachments/assets/44421255-4539-4fde-8231-55089a4f7aae" />


[You can see & interacte with Dashboard live from here](https://app.powerbi.com/view?r=eyJrIjoiYWYyYzlkNWItYTkwZC00OGUyLThlNWItM2FmYmNiYzI4YTM5IiwidCI6IjJiYjZlNWJjLWMxMDktNDdmYi05NDMzLWMxYzZmNGZhMzNmZiIsImMiOjl9) 

## Project Overview
This project delivers a comprehensive, end-to-end data analytics and predictive modeling solution designed to analyze and forecast customer churn within the banking sector. By transforming raw operational data into actionable business intelligence, the project provides a strategic framework for improving customer retention.

The solution encompasses the entire data lifecycle: from data extraction, rigorous cleaning, and relational data modeling, to the deployment of an advanced machine learning algorithm (XGBoost) optimized to identify hidden patterns of at-risk accounts. The final deliverable is an interactive, executive-level Business Intelligence dashboard structured into three strategic tiers: Demographic Overview, Customer Behavioral Analysis, and Predictive Analytics. This allows stakeholders to transition from reactive reporting to proactive, data-driven decision-making, ultimately safeguarding revenue and enhancing customer lifetime value.

## Business Problem
Customer churn is a major challenge for the bank, leading to a direct loss of revenue and shrinking market share. In the banking industry, acquiring a new customer is significantly more expensive than retaining an existing one.

Currently, the bank operates reactively. Management only realizes a customer is unhappy after they have already closed their account and left. The bank lacks a clear understanding of the key factors driving customers away (such as inactivity, age, or account balance). More importantly, they do not have a system to identify at-risk customers in advance. Without knowing why customers leave and who is likely to leave next, the bank cannot take proactive steps to save these relationships, resulting in millions of dollars in potential lost value.

## Questions to Answer
To solve the business problem, this project was designed to answer the following key questions:
* What are the demographic profiles (age, gender, and location) of the customers who are most likely to leave the bank?
* How does general customer behavior, such as the number of bank products used, influence their decision to stay or leave?
* How do customer churn rates and activity levels (active members percentage) trend over their years with the bank (tenure)?
* Is there a relationship between a customer's credit level and their likelihood of leaving?
* Which specific customers are currently at the highest risk of closing their accounts in the near future?
* What is the total financial value (total account balances) that the bank is at risk of losing if these high-risk customers are not retained?

## Model Performance & Business Impact
To transition from descriptive statistics to actionable foresight, an XGBoost machine learning model was developed. Given the natural imbalance in churn data, SMOTE (Synthetic Minority Over-sampling Technique) was applied to ensure the model could accurately detect the minority class (churners) without bias.

**Evaluating Success in Business Terms:**
Rather than relying solely on overall accuracy, the model was evaluated based on its ability to catch churning customers before they leave (the 'Recall' metric). 
* **Business Translation:** For every 100 customers who are actually planning to leave the bank, our predictive model successfully identifies and flags **[XX]** of them in advance. 
* This high capture rate gives the bank a massive window of opportunity to intervene and retain the vast majority of its at-risk clients.

**Model Outputs:**
The model successfully learned the complex patterns of customer behavior. Below is the Feature Importance output, demonstrating which factors the model heavily relied on to make its predictions (such as Age or Account Inactivity):


<img width="698" height="455" alt="Feature Importance" src="https://github.com/user-attachments/assets/f372677e-37dd-43ae-8652-4d996f621ea9" />
)`

**How This Helps the Bank:**
Instead of a simple "Yes/No" prediction, the model outputs a definitive **Churn Probability Score (0% to 100%)** for every active customer. 
* Customers with a probability score of > 80% are automatically flagged as "High Risk".
* This output is fed directly into the Power BI dashboard, allowing the bank to quantify the exact "Value at Risk" (the total balances of these high-risk customers).
* The business impact is immediate: The retention team now has a daily, prioritized target list, enabling them to launch proactive campaigns to save millions of dollars before the customer officially leaves.

## Insights & Recommendations

**Key Insights:**
* **Geographic and Demographic Trends:** Customers located in Germany, as well as middle-aged account holders, exhibit a disproportionately high rate of leaving the bank compared to other segments.
* **Engagement Drop-off:** Account inactivity is a massive driver of churn. Notably, the data reveals a concerning trend: as customers spend more years with the bank (higher tenure), their active engagement tends to drop, which in turn steadily increases their likelihood to leave.
* **Product Overload:** While having multiple products usually implies loyalty, the data shows that customers holding 3 or 4 bank products have an alarmingly high churn rate (reaching near 100% for 4 products). This indicates a severe issue with the service experience or fee structure for multi-product clients.
* **Predictive Risk:** A specific, identifiable segment of the current customer base is at "High Risk" of leaving (probability > 80%), representing a significant amount of the bank's total financial value at risk.

**Business Recommendations:**
* **Targeted Intervention:** Distribute the AI-generated "High-Risk" list to the customer success team daily. Prioritize immediate phone calls and personalized retention offers for these specific clients to protect the millions of dollars currently at risk.
* **Re-activation Strategy:** Do not take long-term customers for granted. Launch automated re-engagement campaigns targeting older accounts that show early signs of inactivity, offering incentives to log in or use their cards.
* **Investigate Multi-Product Experience:** Conduct an immediate review of the customer journey for clients holding 3 or 4 products. Identify and resolve the hidden pain points—whether they are hidden fees, poor customer support, or complicated interfaces—causing these heavily invested customers to leave.

## Types of Analysis Performed
This project utilizes a full spectrum of data analytics to provide a complete and actionable view of the business:
* **Descriptive Analysis (What happened?):** Summarizing historical data to understand current customer demographics, total account balances, and overall churn rates across different regions.
* **Diagnostic Analysis (Why did it happen?):** Exploring behavioral data to identify the root causes of churn, such as uncovering how account inactivity and holding multiple bank products negatively impact customer loyalty.
* **Predictive Analysis (What will happen?):** Applying machine learning algorithms (XGBoost) to forecast future behavior, specifically calculating a definitive churn probability score for every active customer.
* **Prescriptive Analysis (What should we do?):** Transforming these predictions into a strategic action plan, such as providing a prioritized "High-Risk" list for the customer success team to target with immediate retention campaigns.

## Tools Used
To execute this end-to-end data project effectively, a robust stack of analytical, design, and business intelligence tools was utilized:
* **UI/UX Design & Wireframing:** Figma for designing the dashboard layout, user flow, and overall visual theme prior to development, ensuring a seamless and intuitive user experience.
* **Data Processing & Manipulation:** Python (Pandas, NumPy) for rigorous data cleaning, transformation, and exploratory data analysis.
* **Machine Learning & Predictive Modeling:** Python (Scikit-Learn, XGBoost) to develop and train the predictive churn model. SMOTE (Synthetic Minority Over-sampling Technique) was applied to address data imbalance and ensure accurate predictions for the minority class.
* **Business Intelligence & Visualization:** Microsoft Power BI was used as the primary platform for relational data modeling, DAX measure creation, and developing the final interactive, executive-level dashboards.
