# MIST 4610 Group Project 2: Global Cybersecurity Threat Analysis with Tableau​

## Group 3, Section 21482

Team Members:
- Tyson Elmore [@TysonElmore](https://github.com/TysonElmore)
- Matthew Liu [@marshy6](https://github.com/marshy6)
- Lucas Luxemburger [@lucasjbluxemburger](https://github.com/lucasjbluxemburger)
- Gabe Po [@gabepo](https://github.com/gabepo)
- Chris Trinh [@cat35795](https://github.com/cat35795)

## Dataset Description

For this project, we used the dataset “Global_Cybersecurity_Threats_2015-2024.csv” from [Kaggle](https://www.kaggle.com/datasets/atharvasoundankar/global-cybersecurity-threats-2015-2024). It covers cybersecurity incidents from 2015 through 2024 and gives a broad look at how different types of attacks have impacted industries over time.

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

## Q1: Which attack type is hurting us the most?
Question: "We're a healthcare organization that has experienced several cyber incidents. Based on industry data, which attack types are causing the greatest financial damage and affecting the most patients — and where should we be focusing our security budget?" 

### Why It's important: 

In healthcare, cyberattacks don't just cause financial harm — they can delay patient care, expose sensitive medical records, and put lives at risk. Understanding which attack types carry the greatest combined burden allows healthcare organizations to make better decisions that protect both their finances and their patients.

The visualization for this question ties into the dataset by using Attack Type, Financial Loss, Number of Affected Users, and filtering for the Healthcare industry, allowing for a focused and data-driven analysis of risk. By plotting total financial loss against total users affected per attack type, the visualization identifies which attacks are most damaging across both dimensions at once.

## Q2: How should we defend ourselves from that attack?
Question: “Given that malware is a leading cyber threat to the healthcare industry, which defense mechanisms most effectively mitigate these attacks, and where should healthcare organizations prioritize their cybersecurity investments?”

### Why It's important: 

Identifying the worst threat is only half the problem — knowing how to defend against it is what drives actionable decisions. With healthcare organizations facing budget constraints and increasing regulatory scrutiny around data protection (HIPAA, etc.), investing in the wrong defense tool wastes resources and leaves critical systems vulnerable. This question has direct implications: faster incident resolution and lower financial loss per incident means more resources available for patient care and less disruption to hospital operations.

This question uses the dataset's Defense Mechanism Used, Incident Resolution Time (in Hours), Financial Loss (in Million $), Attack Type, and Target Industry columns. By first ranking all defense tools by average resolution time (filtered to Malware/Healthcare), then comparing the top performers by average financial loss per incident, the visualization produces a two-dimensional recommendation grounded in both speed and cost-effectiveness.

## Manipulations applied to the dataset as apart of our analysis:

While no data cleaning or structural changes were required, several filtering and aggregation steps were applied to prepare the data for each question.

For Question 1, the dataset was filtered to include only incidents from the Healthcare industry. Financial Loss and Number of Affected Users were then aggregated by Attack Type using a SUM, allowing for a direct comparison of total impact across attack types on both dimensions.

For Question 2, the dataset was filtered to the Healthcare industry and further narrowed to Malware incidents specifically, as Q1 identified Malware as the highest-risk attack type. Incident Resolution Time was aggregated by Defense Mechanism using an AVERAGE, enabling a fair comparison of how efficiently each tool responds to malware incidents. Average Financial Loss per incident was also calculated per Defense Mechanism to go beyond resolution speed and determine which of the top-performing tools delivers the most cost-effective defense against malware.

## Analysis and results: 

### Q1: Which attack type is hurting us the most?

The scatter plot below displays major attack types in the healthcare industry, plotted by total financial loss (y-axis) and total number of users affected (x-axis). The "Select an Industry" dropdown allows the viewer to filter the visualization by industry, making the dashboard applicable beyond healthcare for any organization using this dataset.

<img width="1354" height="893" alt="image" src="https://github.com/user-attachments/assets/e779b8cd-069a-49ec-8535-860985b5d506" />

The visualization reveals that Malware is the most dangerous attack type in the healthcare industry, leading all other attack types in both total financial loss (approximately $4,000M) and total number of patients affected (approximately 45M). This positions Malware clearly apart from the rest of the field across both dimensions, making it the highest-priority threat for healthcare organizations to address.

The implication is direct: healthcare security budgets should be weighted heavily toward Malware defenses, as it represents the greatest combined financial and patient burden of any attack type in the dataset. This finding directly motivates Question 2, which investigates which defense tools are most effective against Malware specifically.

### Q2: How should we defend ourselves from that attack?

The dashboard below displays average incident resolution time for each defense mechanism (top chart) and average financial loss per incident among the three fastest-resolving tools (bottom chart), both filtered to Malware attacks in the Healthcare industry. The "Select Attack Type" dropdown allows the client to switch between attack types to see how defense tool effectiveness changes depending on the threat — making the dashboard useful beyond just Malware for any attack type the organization is concerned about.

<img width="1177" height="885" alt="image" src="https://github.com/user-attachments/assets/2a8b1c82-115d-4704-9371-31f6bd19af2e" />

The analysis identifies AI-based Detection (34.56 hrs), Antivirus (34.90 hrs), and Firewall (34.93 hrs) as the top three performing defense tools based on average incident resolution time. Because the top three perform within less than 0.4 hours of each other, the bottom chart provides further insight to determine the best overall option — revealing that AI-based Detection results in the lowest average financial loss per incident ($51.4M), compared to Antivirus ($53.7M) and Firewall ($54.9M).

The overall implication is that healthcare organizations should prioritize investment in AI-based Detection when defending against Malware. It is the fastest-resolving tool and produces the lowest financial damage per incident, making it the most cost-effective defense option across both metrics.
