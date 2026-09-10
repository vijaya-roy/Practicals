# Practical 5: Anonymization Techniques

## Aim

To understand different data anonymization techniques such as k-anonymity, differential privacy and data masking, and apply them to a sample real-world dataset.

## Introduction

Data anonymization is the process of modifying personal data so that individuals cannot be easily identified. It helps organizations use data for analysis while reducing privacy risks.

## Anonymization Techniques

### 1. K-Anonymity

K-anonymity ensures that each individual in a dataset is indistinguishable from at least **k-1 other individuals** based on selected identifying attributes.

For example, if **k = 3**, every combination of quasi-identifiers should represent at least three individuals.

### 2. Differential Privacy

Differential privacy adds controlled statistical noise to query results so that information about any individual cannot be easily identified.

**Example:** Adding a small amount of noise to the number of students who answered a survey.

### 3. Data Masking

Data masking replaces or hides sensitive information while keeping the data useful for its intended purpose.

**Example:**

```text
Original Email: vijaya123@gmail.com
Masked Email:   v*****@gmail.com

Sample Dataset

| Name | Age | City   | Email                             |
| ---- | --: | ------ | --------------------------------- |
| A    |  21 | Delhi  | [a@gmail.com](mailto:a@gmail.com) |
| B    |  22 | Delhi  | [b@gmail.com](mailto:b@gmail.com) |
| C    |  21 | Mumbai | [c@gmail.com](mailto:c@gmail.com) |
| D    |  23 | Mumbai | [d@gmail.com](mailto:d@gmail.com) |

Applying Anonymization

After anonymization, direct identifiers such as names and complete email addresses can be removed or masked.

| Age Group | City   | Masked Email     |
| --------- | ------ | ---------------- |
| 20-22     | Delhi  | a*****@gmail.com |
| 20-22     | Delhi  | b*****@gmail.com |
| 20-22     | Mumbai | c*****@gmail.com |
| 23-25     | Mumbai | d*****@gmail.com |

Here, Name is removed, Age is generalized into age groups, and Email is masked.

Privacy Benefits
Reduces the possibility of identifying individuals.
Protects sensitive personal information.
Allows data to be used for analysis with reduced privacy risk.
Helps organizations follow data protection principles.

Limitations
Excessive anonymization can reduce the usefulness of data.
Poor anonymization may still allow individuals to be re-identified.
Differential privacy requires careful selection of the amount of noise.
Anonymized data should still be protected from unauthorized access.

Result
K-anonymity, differential privacy and data masking were studied and applied to a sample dataset to reduce the risk of identifying individuals.

Conclusion
Data anonymization helps balance data utility and privacy. Techniques such as k-anonymity, differential privacy and data masking can reduce privacy risks when personal data is used for analysis or shared with others.
