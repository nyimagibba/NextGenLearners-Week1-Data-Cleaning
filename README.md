# Applicant Data Cleaning and Exploration Using Python

### NextGenLearners Internship Program | Week 1 Project

## Project Overview

This project was completed as part of the **NextGenLearners Internship Program**, focusing on the fundamentals of data cleaning, preprocessing, and exploratory data analysis using Python.

The primary objective was to identify and resolve common data quality issues in an applicant dataset, ensuring that the information is accurate, consistent, and suitable for further analysis.

The project involved examining missing values, identifying duplicate records, standardizing inconsistent entries, correcting formatting issues, and validating the cleaned dataset.

## Dataset Description

The project uses a **simulated applicant dataset created for educational and practical training purposes**. The dataset represents individuals applying for internship opportunities across different technology-related fields.

The original dataset contained **80 applicant records and 7 columns**.

| Column | Description |
|---|---|
| Applicant Name | Full name of the applicant |
| Email | Applicant's email address |
| Phone | Applicant's contact number |
| Domain Applied | Technology field selected by the applicant |
| University | Applicant's educational institution |
| Application Date | Date the application was submitted |
| Status | Application review status |

**Dataset Source:** Simulated applicant data used for educational purposes. The records are not presented as actual applications submitted to NextGenLearners.

## Tools and Technologies

- **Python:** Data cleaning and processing
- **Pandas:** Data manipulation, exploration, and validation
- **Google Colab:** Development and execution environment
- **GitHub:** Project documentation and sharing

## Data Cleaning Methodology

### 1. Initial Data Exploration

Loaded the dataset using Pandas and examined its structure, data types, missing values, and duplicate records.

Key functions used:

- `pd.read_csv()`
- `df.head()`
- `df.info()`
- `df.isnull().sum()`
- `df.duplicated().sum()`

### 2. Handling Missing Values

Identified incomplete records and applied appropriate cleaning decisions.

- Removed one record with a missing applicant name.
- Replaced missing email information with `Not Provided`.
- Replaced missing university information with `Not Specified`.
- Assigned `Under Review` to the missing application status.

These decisions helped preserve useful records while addressing incomplete information.

### 3. Removing Duplicate Records

Identified and removed four exact duplicate records using Pandas.

Additional checks were performed on email addresses to identify potential duplicate applications.

### 4. Standardizing Text and Categories

Improved consistency across categorical and text-based columns.

- Removed unnecessary whitespace from applicant names.
- Standardized capitalization and formatting.
- Converted email addresses to lowercase.
- Standardized university names.
- Consolidated internship domains into five consistent categories.
- Standardized application statuses into three categories: `Selected`, `Rejected`, and `Under Review`.

### 5. Cleaning Application Dates

Converted the Application Date column into a datetime format using `pd.to_datetime()`.

One invalid date was identified and retained as a missing date (`NaT`) to avoid introducing inaccurate information.

### 6. Cleaning Phone Numbers

Standardized phone number formatting by removing unnecessary spaces and hyphens while preserving the phone numbers as text.

### 7. Final Data Quality Validation

Performed a final review of the cleaned dataset to confirm record counts, duplicate removal, missing values, standardized categories, and date conversion.

## Data Cleaning Results

| Metric | Before Cleaning | After Cleaning |
|---|---|---|
| Total Records | 80 | 75 |
| Total Columns | 7 | 7 |
| Exact Duplicate Records | 4 | 0 |
| Missing Applicant Names | 1 | 0 |
| Missing Application Dates | Invalid date present | 1 (`NaT`) |
| Domain Categories | 7 | 5 |
| Application Status Categories | Inconsistent formatting | 3 |

**Final Dataset:** 75 applicant records with 7 columns.

The cleaned dataset was exported as `applicants_cleaned.csv`.

## Project Files

| File | Description |
|---|---|
| `Week1_Data_Cleaning_Nyima.ipynb` | Google Colab notebook containing the data cleaning process, Python code, and explanations |
| `applicants_cleaned.csv` | Final cleaned applicant dataset |
| `README.md` | Project overview, methodology, and results |

## Skills Demonstrated

Through this project, I developed and applied practical skills in:

- Data exploration and quality assessment
- Handling missing and invalid values
- Duplicate detection and removal
- Data standardization and transformation
- Working with Pandas DataFrames
- Date and text processing
- Data quality validation
- Technical documentation

## Key Learning Outcomes

This project strengthened my understanding of the importance of data preprocessing in the data analytics workflow.

I learned that effective data cleaning involves more than removing errors. It requires making thoughtful decisions about incomplete records, preserving useful information, maintaining consistency, and documenting each transformation.

I also gained experience using Python and Pandas to prepare a structured dataset for future analytical tasks.

## Conclusion

Completing this project provided practical experience in transforming a dataset with quality issues into a cleaner and more consistent format.

The experience reinforced the importance of data quality in producing meaningful and reliable analytical results.

This project represents the first stage of my practical learning journey through the **NextGenLearners Internship Program**.

---

**Program:** NextGenLearners Internship Program  
**Project:** Week 1 — Foundations: Cleaning and Exploring the Applicant Dataset  
**Technologies:** Python | Pandas | Google Colab | GitHub
