# UPI-Transaction-Analysis-Dashboard

### Dashboard Link:https://app.powerbi.com/links/0sksSM3dpM?ctid=3ad87f0e-1f93-41bd-94f4-82c37d971c88&pbi_source=linkShare

## Problem Statement

This dashboard provides a comprehensive analysis of Unified Payments Interface (UPI) transactions to understand user behavior and identify key trends in the digital payments landscape. The objective is to visualize critical metrics such as total transaction value, volume, and average transaction amount. The report delves into transaction patterns by type (e.g., Peer-to-peer, Merchant payments), user demographics (age, gender), and performance across different banks and locations. These insights can help financial institutions and businesses optimize their services and marketing strategies.

### Steps Followed

-   **Step 1:** Loaded the UPI transaction dataset into Power BI Desktop.
-   **Step 2:** Used Power Query Editor for data cleaning, checking data types, and ensuring data integrity.
-   **Step 3:** A custom theme was applied to maintain a consistent and professional look for the dashboard.
-   **Step 4:** Added a **Date Slicer** to the canvas to allow users to filter the report for specific time periods.
-   **Step 5:** Created a DAX **Calculated Column** to segment customers into distinct age groups for demographic analysis. The following DAX expression was used:
    ```dax
    Age group = If('UPI Transaction'[CustomerAge]<=24,"A1",IF('UPI Transaction'[CustomerAge]<=35,"A2","A3"))
    ```
-   **Step 6:** Developed several DAX **Measures** to calculate the main KPIs for the dashboard.
    ```dax
    Total Amount = SUM('UPI Transaction'[Amount])
    ```
    ```dax
    Total Transaction = COUNT('UPI Transaction'[TransactionID])
    ```
    ```dax
    Average Amount = AVERAGE('UPI Transaction'[Amount])
    ```
-   **Step 7:** Used **Card** visuals to prominently display the key KPIs: "Total Amount," "Total Transaction," and "Average Amount." Additional cards were used for "Male Customers" and "Female Customers."
-   **Step 8:** Designed the report with a variety of visuals:
    -   **Donut Charts** to show the distribution of "Total Amount by Transaction Type," "Total Amount by Gender," and "Total Amount by Transaction Status."
    -   **Bar Charts** to compare "Total Amount by Bank" and "Total Transaction by Age group."
    -   A **Map** visual to illustrate "Total Amount by Location."
    -   A **Line Chart** to show the trend of "Total Amount by Month."
-   **Step 9:** Published the final report to the Power BI Service for sharing and collaboration.

---

# Snapshot of Dashboard
<img width="1411" height="742" alt="Screenshot 2025-09-22 193557" src="https://github.com/user-attachments/assets/ceb82dec-bb59-4fa1-a2eb-a1657b64780d" />
<img width="1417" height="750" alt="Screenshot 2025-09-22 193536" src="https://github.com/user-attachments/assets/c60e46a1-f1b3-4796-8cb0-449cc57458cb" />



---

# Insights

This dashboard reveals key trends and user behaviors within the UPI transaction data.

### [1] Top-Level KPIs

-   **Total Transaction Amount:** ₹1.2 Crore
-   **Total Number of Transactions:** 2.1K
-   **Average Transaction Amount:** ₹5.7K

### [2] Transaction Behavior & Trends

-   **Transaction Types:** **Bill Payments** constitute the largest portion of the total transaction amount, followed by Peer-to-peer and Merchant payments.
-   **Top Banks:** **HDFC Bank** leads in transaction value, with **ICICI** and **SBI** being the next top performers.
-   **Transaction Status:** The vast majority of transactions are successfully **Completed**, indicating a high reliability of the payment system.
-   **Monthly Trend:** The line chart shows fluctuations in transaction amounts over time, allowing for the identification of peak months.

### [3] Demographic Insights

-   **Gender Distribution:** The user base is almost evenly split, with **260 Male** and **240 Female** customers. However, males contribute slightly more to the total transaction amount.
-   **Age Group Analysis:** The **A2 age group (25-35 years)** is the most active segment, accounting for the highest number of transactions. This suggests that young professionals and millennials are the primary users of the UPI platform.
