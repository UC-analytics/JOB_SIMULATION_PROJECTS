# :purple_square: Deloitte Australia Data Analytics Job Simulation on Forage  

In this project, I worked as a data analyst in the Deloitte team to provide insights to a customer and help to guide their decision making, using tools such as Tableau and Excel. This project was executed based on a real-world context.

---

## :clipboard: Project Overview

The first client, Macura Industries, uses technology to track data from their factories. For this project, I was required to analyze their telemetry data in order to identify the key issues that were affecting their operations and causing interruptions on the assembly line. 
For a second client, Daikibo industries, a concern was raised concerning a worrisome number of internal complaints received regarding inequality in terms of salary, and I was recruited to help them investigate the issue using data gotten from an algorithm built by the forensic tech team, to quantify the levels of gender pay equality across the company's major job roles and its different locations. 

---

## :interrobang: Problem Statement

Macura Industries:
-	In which location did machines break the most?
-	What are the machines that broke most often in that location?

Daikibo Industries:
-	Address the gender pay gap in the organization
-	Categorize the discrepancies into: "fair", "unfair" and "highly discriminative"

---

## :hammer_and_wrench: Tools & Packages

This project was done in Using Tableau and Excel.

---

## :microscope: Methodology

### TASK 1: Macura Industries
The dataset used was provided by Deloitte, in a JSON format. 
- I imported it into my tableau workspace, making sure to check all schema levels
- Created a calculated field to label numerically the instances where the company suffered a downtime in data transmission
  ``` IF [STATUS] = "unhealthy" THEN 10 ESLE 0 END ```
- Created a classic bar chart to show the downtime levels per factory locations and named it "Downtime per factory"
- Created another classic bar chart to show the machines that were implicated every time there was a downtime and named it "Downtime per device"
- Created a dashboard combining the two charts for side-by-side evaluation
- Created a filter using the downtime per factory chart to narrow my findings down to specific locations of the company


### TASK 2: Daikibo Industries
The dataset used was provided by Deloitte, in an XLSX format.
- I created a working copy of the dataset for my analysis
- Perused the data, while ensuring it was cleaned
- Created a calculated column using an "IFS statement" to categorize the salary inequality levels using the data from the "Equality Score" column
  ```=IF(AND(C2>=-10,C2<=10),"Fair", IF(OR(C2<-20,C2>20),"Highly Discriminative", "Unfair"))```
- Copied the new column, pasted it as a value into a new column and named it "Equality Class"

---

## :bulb: Key Findings & Insights
-	:chart: **Macura Industries**:
  - The factory that is experiencing the most downtimes is the one in Seiko, Japan. Its most compromised device causing this is the Laser Welder
  - While the factory in Shenzhen, China follows closely behind, its problematic machine is the Laser Cutter
  - The Laser Cutter and the Heavy-Duty Drill are what contribute to the downtime in Meiyo, but this is significantly less than that of Schenzehn and Seiko
  - The factory with the least number of downtimes is the Berlin factory in Germany. The device of interest here is the furnace machine

<img width="1340" height="823" alt="Dashboard 1" src="https://github.com/user-attachments/assets/c5ac360f-4914-4163-ad04-48c9c058b660" />

-	:construction_worker_woman: **Daikibo Industries**:
  - The salaries of about 7 employees were found to be highly discriminative, 11 were unfair, and 19 of them were fair.
  - So only approximately 51% of employees were being paid fairly. The concerns were valid.

<img width="1911" height="1042" alt="Daikibo" src="https://github.com/user-attachments/assets/e5eb3229-97d3-47d6-920c-2eb944b500cc" />


---

## :warning: Limitations

### Current Limitations
- This project was limited only to the demands of the project, much more analysis could be done, and more inferences drawn from the data provided
- Other factors that may affect the pay gap in Daikibo industries were not factored. For example the employees' experience level, the cost of living across the various locations, gender representation in various job segments, and pay secrecy of some of the employees.
- This analysis is descriptive, not predictive

---

## :mailbox: Contact

**Uchechukwu Esther Okwudili**  
:e-mail: ucokwudili27@gmail.com  
:briefcase: www.linkedin.com/in/uchechukwu-okwudili-a7437933a  
:globe_with_meridians: 

---

*⭐ If you found this project useful or interesting, feel free to star the repository!*
