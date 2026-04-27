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

To answer this question, the dataset was filtered to only include incidents from the Healthcare industry and where the attack type was Malware.

The Resolution Time variable was then aggregated by calculating the average resolution time for each Defense Mechanism. This allowed for a direct comparison of how efficiently each defense responds to malware incidents.

No major data cleaning was required beyond filtering and aggregation, as the dataset was already structured appropriately for analysis.



## Analysis and results: 

Q1 Visualization: 
<img width="626" height="404" alt="image" src="https://github.com/user-attachments/assets/0454a4a9-d0d5-461b-8c05-5d92390866fd" />


Q1: Healthcare Attack Types by Financial Loss and Users Affected

Visualization Analysis:
The scatter plot illustrates a strong positive correlation between the number of affected users and total financial loss.

Primary Threat (High Impact/High Loss): Malware sits at the top-right corner of the plot, causing over $41 million in losses and impacting approximately 43 million users. This indicates that malware is not just a frequent nuisance but also a systemic risk to healthcare infrastructure.

Secondary Threats: DDoS and Ransomware follow closely. While Ransomware is often the most publicized, this data suggests that the immense volume of users disrupted by DDoS attacks leads to comparable financial repercussions (roughly $38 million).

Targeted Threats: Man-in-the-Middle (MitM) and Phishing show lower relative impact but still account for significant losses, typically affecting 28M–32M users.

Implications:
The healthcare industry is particularly vulnerable because of the high "value per record." Since malware and DDoS sit in the highest quadrant, the organization should prioritize redundancy and endpoint protection. This data suggests that for every 1 million additional users affected, the financial loss increases linearly, implying that containment is just as important, if not more, as prevention.

Q2 Visualization: 
<img width="564" height="429" alt="image" src="https://github.com/user-attachments/assets/c6aeb5d2-5756-42ab-b350-04165f768aa7" />

Q2: Best Defense Tools (Avg. Hours to Resolve Incident)

Analysis of Defense Effectiveness:
To address the primary threats identified in Q1, we analyzed which defense mechanisms yielded the lowest resolution time. In a healthcare setting, every hour of downtime can equate to compromised patient care and increasing recovery costs.

Visual Data Findings (DDoS Filtered):

Top Performer: Encryption is the most efficient defense tool, with an average resolution time of 21.50 hours. This data suggests that protected data is significantly easier to recover and/or verify during a breach.

Middle Tier: Antivirus falls second with a resolution time of 35.00 hours.

Lower Efficiency: VPNs (41.80 hours), AI-based Detection (42.00 hours), and Firewalls (42.75 hours) show the longest resolution times. While these tools are essential for prevention, the data indicates they may not be the fastest tools for resolution once an incident has occurred, although these can be some of the stronger defense tools. 

Implications:
Given that Malware and DDoS are leading threats, the budget should shift toward tools that minimize downtime. While AI-based detection is a growing modern investment, its higher resolution time (42.00 hours) show that companies might want to pair it with more aggressive automated response protocols to be effective. Investing in robust encryption should be a top priority, as it currently results in the fastest return to normal operations.


## Tableau Packaged Workbook
