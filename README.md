# Govern-Heart-Data
Data Governance Implementation on UCI Heart Disease Dataset
Description: This project implements key data governance techniques to ensure the security, privacy, and compliance of the UCI Heart Disease dataset. The primary goal is to safeguard sensitive patient information while enabling efficient data analysis for heart disease prediction. The project applies advanced methods such as access control, anonymization, and pseudonymization to protect and manage the data. These methods are essential in maintaining data integrity, preventing unauthorized access, and adhering to ethical and regulatory standards.

**Project Structure**: 
-DataProcessing.py: Handles data cleaning, identifying and addressing missing values, duplicates, and outliers, and applying anonymization and pseudonymization techniques.
-AccessControl.py: Implements the access control mechanisms, defining roles and permissions for various users.
-DataValidation.py: Ensures data quality through validation frameworks like Pandera and Great Expectations.

DataProcessing.py
This script is responsible for the main data governance tasks, focusing on cleaning and securing the dataset. The following techniques were used:

# Anonymization:
-Randomization: Applied to the "Chest Pain Type" (cp) column, randomizing the values to obscure individual patient details while preserving the overall data structure for analysis.
-Generalization: Used on the "Age" column, grouping patient ages into broader categories (e.g., 30-40, 40-50) to prevent identification while maintaining data utility for trend analysis.
-Masking: Sensitive columns such as "ID" and "dataset" were masked by replacing them with pseudo-random identifiers to prevent direct identification of individuals.
-Perturbation: Noise was added to numerical values like "Resting Blood Pressure" and "Cholesterol" to protect privacy while preserving statistical integrity.

# Pseudonymization:
-Scrambling: Labels in the dataset were scrambled to prevent tracing individual records to their original sources, enhancing privacy.
-Hashing: Cryptographic hashing was used on sensitive data such as "Resting Electrocardiographic Results" (restecg) to create irreversible transformations, allowing secure storage and analysis without compromising -confidentiality.
-Encryption: The "Gender" (sex) column was encrypted using a cryptographic algorithm, ensuring secure data transmission and storage while preserving the confidentiality of sensitive attributes.



# AccessControl.py
This script implements Mandatory Access Control (MAC) to enforce strict security policies, ensuring that only authorized users have access to sensitive information. The MAC model operates under predefined rules established by the system administrator, providing enhanced security and regulatory compliance. Key features include:

High Security: MAC enforces stringent access rules that cannot be modified by regular users, making it ideal for environments requiring high data security, such as healthcare.
Centralized Management: Administrators have full control over access permissions, simplifying security management and ensuring consistent application of policies across the dataset.
Preventing Data Leakage: By strictly regulating who can access specific data, MAC reduces the risk of unauthorized access and potential data breaches, protecting patient confidentiality.
Regulatory Compliance: MAC helps ensure compliance with regulations like HIPAA by limiting data access to only those individuals with the proper clearance, maintaining data integrity and confidentiality.

# DataValidation.py
This script ensures that the processed dataset meets high-quality standards using:

Pandera: For schema validation, ensuring that the dataset conforms to predefined structures, such as data types and value ranges.
Great Expectations: For defining and validating expectations around the dataset's content and structure, helping catch potential data issues early.





# Security:
Security in this project is enforced through a combination of anonymization, pseudonymization, and access control techniques. Sensitive attributes such as age, chest pain type, and gender are anonymized and pseudonymized to prevent re-identification of individuals, while cryptographic algorithms ensure the integrity and confidentiality of the data.
The use of Mandatory Access Control (MAC) ensures that only authorized personnel have access to the data. This is especially important in medical data handling, where unauthorized access could lead to privacy violations or data breaches. The MAC system provides a high level of security by enforcing strict, centralized access rules that prevent data leakage and insider threats.


