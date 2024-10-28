This project is the realization of https://github.com/banggaadi/Resume-Clustering-with-NER project
# Data Science Job Requirement Analysis
This project aims to analyze the job requirements for data scientist roles by examining job postings from an online job portal (JobStreet.com). Through this analysis, I sought to identify the skills, experience, and qualifications most frequently required for data science roles. Additionally, I developed a scoring system to evaluate LinkedIn profiles of data scientists, measuring how well they meet these industry requirements.

## Project Overview
### Data Collection
I used BeautifulSoup to scrape job posting data from JobStreet.com, focusing on positions with the title "Data Scientist." The dataset includes information about job requirements, qualifications, and descriptions for 128 data scientist roles.
![image](https://github.com/user-attachments/assets/fb154db7-a043-42ea-a7c2-2984135508ce)


### Skills and Experience Extraction

1.To identify specific skills required for these roles, I trained a Named Entity Recognition (NER) model using a dataset from Mendeley Data. This model was used to extract technical skills from the job descriptions.

![image](https://github.com/user-attachments/assets/b5e9a217-55dd-423d-a4cd-282f3dcc56ed)
Note: The dataset for the NER model categorizes skills into three classes—Hardskill, Softskill, and Techskill. For this project, I focused on Techskills to extract specific technical skills required in job descriptions.

2.I used regular expressions (regex) to identify and extract minimum required experience for each position.

![image](https://github.com/user-attachments/assets/2513050d-997a-4004-aff2-5c53e1759405)
This is the final form of the job requirement data after extracting skills and experience.

3.I collected LinkedIn data from data scientists currently employed in the field with third-party API, extracting their skills, experience, and education level. Based on these factors, I created a scoring system to assess how well each profile aligns with industry requirements. The LinkedIn data size is profiles

### Scoring Methodology
The scoring system uses a 100-point scale, with the following weight distribution:

Skills: 55%

Experience: 35%

Education: 10%

![image](https://github.com/user-attachments/assets/5825be65-08a4-470d-b857-b349088d9c0f)

![image](https://github.com/user-attachments/assets/d9a42146-e95d-4c52-a193-99219a594473)

![image](https://github.com/user-attachments/assets/716c2439-d3ed-4ad2-9076-39ccadbb85a7)


This weight distribution reflects the importance of technical skills and real-world experience in data science. While education is valuable, particularly in statistics, data scientists often build their expertise through hands-on experience and practical skill acquisition.

## Results
After scoring each profile, I ranked them based on employability for data science roles. Additionally, I used a Random Forest classifier to categorize candidates based on their profile scores, achieving an accuracy of 1.0. While this high accuracy may suggest a well-fitting model, further testing and validation are necessary to ensure the model’s robustness and generalizability.

For the ranking system this is the result

![image](https://github.com/user-attachments/assets/5d8774ff-be0f-49a5-884c-884a864371a2)

(Tableau dashboard coming soon!!!)

This is the result of random forest classifier

![image](https://github.com/user-attachments/assets/29420944-adf0-4068-a0b9-60eef8f0ac0d)
