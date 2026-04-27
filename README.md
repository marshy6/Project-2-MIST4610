# MIST 4610 Group Project 2: Global Cybersecurity Threat Analysis with Tableau​

## Group 3, Section 21482

Team Members:
- Tyson Elmore [@TysonElmore](https://github.com/TysonElmore)
- Matthew Liu [@marshy6](https://github.com/marshy6)
- Lucas Luxemburger [@lucasjbluxemburger](https://github.com/lucasjbluxemburger)
- Gabe Po [@gabepo](https://github.com/gabepo)
- Chris Trinh [@cat35795](https://github.com/cat35795)

## Dataset Description

For this project, we used the dataset “Global_Cybersecurity_Threats_2015-2024.csv” from Kaggle. It covers cybersecurity incidents from 2015 through 2024 and gives a broad look at how different types of attacks have impacted industries over time.

The dataset has 3,001 rows and 10 columns, where each row represents a single cybersecurity incident. The columns provide details about what kind of attack happened, who it affected, and how it was handled.

### Key Columns

- **Attack Type** – Type of cyberattack (malware, phishing, ransomware)  
- **Industry** – Industry affected (healthcare, banking, IT)  
- **Financial Loss** – Monetary damage caused  
- **Affected Users** – Number of users impacted  
- **Defense Mechanism** – Security used (firewall, antivirus, etc.)  
- **Resolution Time** – Time to resolve the attack  
- **Vulnerability Type** – Type of weakness exploited

The dataset includes a mix of categorical data (like attack type and industry) and numerical data (like financial loss, number of users affected, and resolution time).

Overall, this dataset gives enough detail to explore patterns in cyberattacks and see how effective different security measures are across industries.


## Q1: Healthcare Attack Types by Financial Loss and Users Affected: 
Question: "We're a healthcare organization that has experienced several cyber incidents. Based on industry data, which attack types are causing the greatest financial damage and affecting the most patients — and where should we be focusing our security budget?" 

Visualization: 
<img width="565" height="551" alt="image" src="https://github.com/user-attachments/assets/f573ae2a-8d4c-4f32-8b95-dcb8e2dda8fd" />


### Why It's important: 

This visualization helps healthcare organizations see which cyberattacks cause the most total damage by comparing financial loss and number of affected patients at the same time. It makes it easier to identify which threats have the greatest overall impact and should be prioritized.

It also highlights that the most common attacks are not always the most costly, helping organizations make smarter decisions about where to focus their cybersecurity budget.

It is directly tied to the dataset by using Attack Type, Financial Loss, Number of Affected Users, and filtering for the Healthcare industry, allowing for a focused and data-driven analysis of risk.

## Q2: Best Defense Tools (Avg. Hours to Resolve Incident): 
Question: “Given that malware is a leading cyber threat to the healthcare industry, which defense mechanisms most effectively mitigate these attacks, and where should healthcare organizations prioritize their cybersecurity investments?”

Visualization: 
(Insert)

### Why It's important: 

This visualization helps healthcare organizations understand which security defenses are actually effective against malware, the most common type of cyberattack. By focusing on resolution time, it shows how quickly different defenses can contain and fix an attack, which is critical for reducing damage and downtime.

It also highlights that not all security tools perform equally well, even if they are commonly used or considered advanced. This allows organizations to make smarter, more targeted decisions about where to invest their cybersecurity budget instead of relying on assumptions.

It is directly tied to the dataset by using Defense Mechanism, Resolution Time, and Attack Type, while filtering for Malware and the Healthcare industry to provide a focused and data-driven analysis of defense effectiveness.



## Manipulations applied to the dataset as apart of our analysis:

The dataset was sufficiently organized to where we did not need to perform any additional manipulations or calculations. 



## Analysis and results: 



## Tableau Packaged Workbook
