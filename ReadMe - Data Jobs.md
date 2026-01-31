#### \## Project Overview



In this project, I analysed data-related job postings from 2024 to understand trends in the data job market. While the original dataset is global, I focused my analysis on job postings relevant to India to make the insights more meaningful for a local job-seeker perspective.



This was a Power BI–focused project, where the emphasis was on data cleaning, modelling, and building an interactive dashboard rather than predictive modelling.



#### \## Business Problem



The data job market is large and constantly changing, which makes it difficult for job seekers to clearly understand:



\- Which data roles are in demand



\- What skills employers are looking for



\- How salaries differ across roles and locations



\- How common remote roles and degree requirements are



The objective of this project was to organise and analyse job posting data in a way that answers these questions clearly and practically and present insights through an interactive Power BI dashboard.



#### \## Data



Source: Luke Barousse – Data Jobs Dataset



Year: 2024



Data collection: Scraped from Google job postings across multiple sources



The dataset is global in nature. For this project, I filtered the data to focus on India-specific job postings.



The data follows a star schema, with the following key tables:



job\_postings\_fact



job\_schedule\_dim



skills\_dim



skill\_job\_dim



company\_dim



#### \## Data Cleaning and Preparation



This was a Power BI-centric project, and data cleaning was performed using Power Query.



One of the main challenges was that multiple skills, job schedules were stored in a single row for each job posting in the job\_postings\_fact table. To handle this:



* I extracted individual skills from job postings where multiple skills were listed together.



* Created a separate skills dimension table containing skill id, skill and skill type by extracting distinct skills.



* Split the skills into individual rows and linked them back to job postings using a bridge table (skill\_job\_dim), enabling a one-to-many relationship.



* Similarly, I cleaned the job type information by splitting multiple job types into separate rows for each job ID.



* Removed duplicate job postings.



* Handled inconsistencies in job titles, locations, and skill names.



* Standardised salary fields where possible.



* Median salary values were used to compare yearly and hourly pay in order to minimise the impact of outliers.



* After cleaning, relationships were created between the fact and dimension tables based on the star schema.



#### \## Analysis Approach



The analysis was descriptive and exploratory rather than predictive.



Using Power BI, I:



* Created measures for job counts, median salaries, and skill frequency



* Used parameters to allow dynamic role-based exploration



* Analysed job demand by role, skill, location, and job type



* Compared median yearly and hourly salaries to better understand compensation patterns



* Used slicers and drill-throughs to support deeper role-specific analysis



The goal was to allow users to interact with the data and explore trends rather than present fixed conclusions.



#### \## Dashboard Pages



**Page 1: Job Market Overview**



The first page provides a high-level view of the data job market in India. It focuses on overall demand, salary benchmarks, and skill trends across roles.



This page includes:



* Total job postings and median salary KPIs



* Job distribution by role



* Most in-demand skills



* Median yearly vs hourly salary comparison



* City-wise distribution of job opportunities



This page is designed to give a quick understanding of the overall job market.



**Page 2: Role Deep Dive**



The second page allows users to drill down into a specific data role for more detailed insights.



This page includes:



* Role-specific job counts



* Key skills required for the selected role



* Salary trends over time



* Job type and work-from-home distribution



This view is useful for comparing roles and understanding role-specific requirements.



#### \## Key Insights 

* Data Engineer and Data Analyst roles account for the highest number of job postings.



* The median yearly salary across data roles is around ₹9.6L, with clear variation by role.



* Python and SQL are the most consistently required skills across roles.



* Cloud and big data tools appear more frequently in engineering-focused roles.



* Many job postings do not explicitly mention a degree requirement.



* Remote roles exist but are still less common than on-site opportunities.



* Bengaluru and Hyderabad lead in data job opportunities.



* LinkedIn is the most common platform for data job postings.



#### \## Actions \& Use Cases



This dashboard can be used to:



* Help job seekers identify high-demand data roles in India



* Understand which skills to prioritise while preparing for data roles



* Set realistic salary expectations based on role and location



* Explore opportunities by city, job type, and work-from-home availability



* The dashboard supports career exploration and informed decision-making, not hiring predictions.



#### \## Tools Used



Power BI: - Power Query for data cleaning
          - Data modelling using star schema
          - Measures and parameters
          - Interactive visuals, slicers, and drill-throughs



#### \## Notes \& Limitations



The dataset is based on scraped job postings and may not represent the entire job market.



Salary values are median-based and may not reflect individual offers.



Job seniority is inferred only from information available in postings.





