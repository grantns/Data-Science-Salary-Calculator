# Data Science Salary Calculator

<img width="769" height="336" alt="Data science" src="https://github.com/user-attachments/assets/db4704f0-a302-4457-a53c-43a1bab77835" />  

## Introduction  
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.


## Excel Skills Used  
The following Excel skills were utilized for analysis:

- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation
  
## Data Jobs Dataset
The dataset used for this project contains real-world data science job information from 2023.  

- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills


## Dashboard Build  

📉 Charts  

### 📊 Data Science Job Salaries - Bar Chart  

<img width="623" height="524" alt="image" src="https://github.com/user-attachments/assets/f35c7e65-a031-48f7-9fc4-eea28e281b58" />  


- 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
- 📉 Data Organization: Sorted job titles by descending salary for improved readability.
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.


### Country Median Salaries - Map Chart  

<img width="643" height="390" alt="image" src="https://github.com/user-attachments/assets/c8b7e1d3-05ee-44d3-9fdf-d51e5838797d" />  

- 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
- 📊 Data Representation: Plotted median salary for each country with available data.
- 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.


## 🧮 Formulas and Functions  

💰 Median Salary by Job Titles  

``=MEDIAN(

IF(  
     
      (jobs[job_title_short]=A2)* 
      
      (jobs[job_country]=country)* 
      
      (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
      
      (jobs[salary_year_avg]<>0), 
      
      jobs[salary_year_avg]  
      
)
)``
