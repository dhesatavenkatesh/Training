1. Why is Data Cleaning Important Before ML Training?

Data cleaning is one of the most critical steps in the machine learning pipeline. Real-world datasets often contain missing values, duplicate records, incorrect entries, inconsistent formats, and irrelevant information. If these issues are not addressed before training, the machine learning model may learn incorrect patterns and produce inaccurate predictions.

For example, if employee salary data contains missing values or incorrect salary amounts, a salary prediction model may generate unreliable results. Similarly, duplicate records can bias the model by giving excessive importance to certain observations.

Data cleaning improves data quality, increases model accuracy, reduces noise, and ensures that the dataset accurately represents real-world conditions. A clean dataset enables machine learning algorithms to focus on meaningful patterns rather than errors and inconsistencies.



2. What Happens if Outliers are Ignored?

Outliers are data points that differ significantly from the majority of observations in a dataset. These values may occur because of data entry errors, unusual events, or naturally rare occurrences.

Ignoring outliers can have serious consequences. Outliers can distort statistical measures such as the mean, variance, and standard deviation. For example, if most employee salaries range between ₹30,000 and ₹80,000 but one salary is recorded as ₹10,00,000, the average salary may become misleading.

In machine learning, outliers can negatively impact model performance. Algorithms such as linear regression are highly sensitive to extreme values and may produce inaccurate predictions when outliers are present. Therefore, outliers should be detected, analyzed, and either corrected, removed, or treated appropriately based on the business context.

3. Why Do We Calculate Correlation?

Correlation measures the strength and direction of the relationship between two variables. It helps analysts understand how changes in one variable are associated with changes in another variable.

For example, in an employee dataset, experience and salary often show a positive correlation. As experience increases, salary tends to increase as well. Understanding these relationships helps in feature selection and model building.

Correlation analysis also helps identify redundant features. If two variables are highly correlated, one of them may be removed to simplify the model without losing significant information. Additionally, correlation helps uncover hidden patterns and supports data-driven decision-making.

By understanding relationships among variables, organizations can improve predictive models and gain deeper insights into their data.

4. Why is EDA Important Before Building a Chatbot Knowledge Base?

Exploratory Data Analysis (EDA) is the process of examining and understanding a dataset before using it for machine learning or AI applications. EDA helps identify missing values, duplicate records, inconsistencies, outliers, and data distribution patterns.

When building a chatbot knowledge base, the quality of the stored information directly affects the quality of chatbot responses. If the knowledge base contains duplicate content, outdated information, missing records, or irrelevant documents, the chatbot may generate inaccurate or confusing answers.

EDA helps ensure that the knowledge base is complete, relevant, and well-structured. It also provides insights into content coverage, topic distribution, and data quality. As a result, the chatbot becomes more reliable, accurate, and efficient in responding to user queries.

5. How Can Poor Data Affect an LLM or RAG System?

Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG) systems rely heavily on high-quality data. Poor-quality data can introduce errors, bias, misinformation, and inconsistencies into the system.

If an LLM is trained on inaccurate or incomplete data, it may generate misleading responses. Similarly, a RAG system retrieves information from a knowledge base before generating answers. If the retrieved documents contain outdated or incorrect information, the generated response may also be incorrect.

Poor data can lead to hallucinations, reduced accuracy, lower user trust, and poor overall performance. It can also introduce ethical concerns by spreading biased or misleading information.

Therefore, data cleaning, validation, quality checks, and continuous monitoring are essential for building trustworthy AI systems. High-quality data ensures better retrieval, more accurate responses, and improved user satisfaction.