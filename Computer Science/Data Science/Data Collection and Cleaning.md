![[Pasted image 20231218162034.png]]
## 1. Data Collection:
   - **Definition:**
     - Data collection is the process of gathering raw information or data from various sources, which serves as the foundation for analysis, modeling, and decision-making in data science.

   - **Sources of Data:**
     - **Internal Sources:** Within the organization, such as databases, logs, and transaction records.
     - **External Sources:** Outside the organization, including public datasets, APIs, and web scraping.
     - **Surveys and Questionnaires:** Gathering data directly from individuals or groups.
     - **Sensor Data:** Capturing information from IoT devices and sensors.
     - **Social Media and Text:** Extracting insights from social platforms and textual data.

   - **Considerations in Data Collection:**
     - **Relevance:** Ensure the collected data aligns with the objectives and problem statement.
     - **Accuracy:** Validate the accuracy and reliability of data sources.
     - **Volume:** Assess the quantity of data needed for meaningful analysis.
     - **Ethical Considerations:** Respect privacy and comply with ethical standards in data collection.

   - **Challenges in Data Collection:**
     - **Incomplete Data:** Missing values or gaps in the dataset.
     - **Biases:** Systematic errors introduced during data collection.
     - **Noise:** Random errors or irrelevant information in the data.
     - **Security Concerns:** Protecting sensitive information during collection.

   - **Data Collection Techniques:**
     - **Sampling:** Collecting data from a subset of the population to make inferences about the entire population.
     - **Experimentation:** Conducting controlled experiments to gather data under specific conditions.
     - **Observation:** Collecting data by observing and recording natural phenomena.
     - **Web Scraping:** Extracting data from websites.

## 2. Data Cleaning:
   - **Definition:**
     - Data cleaning, also known as data cleansing or data scrubbing, involves the process of identifying and correcting errors or inconsistencies in datasets to improve their quality and reliability.

   - **Common Data Cleaning Tasks:**
     - **Handling Missing Values:**
       - Imputation: Replacing missing values with estimated or calculated values.
       - Removal: Removing rows or columns with missing values.

     - **Dealing with Duplicates:**
       - Identifying and removing duplicate records to ensure data integrity.

     - **Handling Outliers:**
       - Identifying and addressing data points significantly different from the majority.

     - **Normalization and Standardization:**
       - Scaling numerical features to a standard range for consistency.

     - **Addressing Typos and Inconsistencies:**
       - Correcting errors in text or categorical data to ensure uniformity.

     - **Converting Data Types:**
       - Ensuring that variables have appropriate data types for analysis.

   - **Importance of Data Cleaning:**
     - Enhances the quality and reliability of analysis and modeling results.
     - Reduces the likelihood of making erroneous conclusions or decisions based on flawed data.
     - Improves the performance of machine learning models by providing cleaner input data.

   - **Tools for Data Cleaning:**
     - **Pandas (Python):** A powerful library for data manipulation and analysis in Python.
     - **OpenRefine:** A tool for cleaning and transforming messy data interactively.
     - **Trifacta:** A cloud-based data cleaning and preparation tool with a user-friendly interface.

   - **Best Practices in Data Cleaning:**
     - **Understand the Domain:** Knowledge of the specific domain helps in identifying anomalies and errors.
     - **Document Changes:** Keep a record of all modifications made during the cleaning process.
     - **Iterative Process:** Data cleaning is often an iterative process, requiring multiple passes.

   - **Challenges in Data Cleaning:**
     - **Time-Consuming:** Cleaning large datasets can be time-intensive.
     - **Subjectivity:** Deciding on the best approach to handle certain issues can be subjective.
     - **Impact on Data Volume:** Cleaning may result in the loss of a significant amount of data.