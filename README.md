# Data Science Job Requirement Analysis
This project aims to analyze the job requirements for data scientist roles by examining job postings from an online job portal (JobStreet.com). Through this analysis, I sought to identify the skills, experience, and qualifications most frequently required for data science roles. Additionally, I developed a scoring system to evaluate LinkedIn profiles of data scientists, measuring how well they meet these industry requirements.

## Project Overview
### Data Collection
I used BeautifulSoup to scrape job posting data from JobStreet.com, focusing on positions with the title "Data Scientist." The dataset includes information about job requirements, qualifications, and descriptions for 128 data scientist roles.

### Skills and Experience Extraction

#### Skills Extraction: 
To identify specific skills required for these roles, I trained a Named Entity Recognition (NER) model using a dataset from Mendeley Data. This model was used to extract technical skills from the job descriptions.
#### Experience Extraction: 
I used regular expressions (regex) to identify and extract minimum required experience for each position.
LinkedIn Profile Scoring
I collected LinkedIn data from data scientists currently employed in the field, extracting their skills, experience, and education level. Based on these factors, I created a scoring system to assess how well each profile aligns with industry requirements.

### Scoring Methodology
The scoring system uses a 100-point scale, with the following weight distribution:

Skills: 55%

Experience: 35%

Education: 10%

This weight distribution reflects the importance of technical skills and real-world experience in data science. While education is valuable, particularly in statistics, data scientists often build their expertise through hands-on experience and practical skill acquisition.

## Results
After scoring each profile, I ranked them based on employability for data science roles. Additionally, I used a Random Forest classifier to categorize candidates based on their profile scores, achieving an accuracy of 1.0. While this high accuracy may suggest a well-fitting model, further testing and validation are necessary to ensure the model’s robustness and generalizability.
