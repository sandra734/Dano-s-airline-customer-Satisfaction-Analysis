# Dano's Airline-customer-Satisfaction-Analysis

## Project Overview 
This project focuses on analyzing customer satisfaction data to identify key drivers of customer happiness and areas for improvement. By examining feedback, survey responses, and other relevant data, the analysis aims to uncover trends, patterns, and insights that can inform strategic decisions. The ultimate goal is to enhance customer experiences, increase loyalty, and improve overall business performance. Key deliverables include visualized reports, actionable recommendations, and a comprehensive understanding of customer sentiment.

### Data Sources 
The data used for this analysis is "Airline data - airline_passenger_satisfaction.csv" [View](https://docs.google.com/spreadsheets/d/15Kp-2yfQFNRGJPNOkpMwG-OMX8xVZOJ5VL7f35v7sRQ/edit#gid=1647986900)

###  Tools
- Excel for Data cleaning and exploration
- Power BI for Data Modeling, Analysis, and Visualization.
    - [Download Here](https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads)+

### Data Cleaning and preparation
- Data loading and inspection 
- Checked for duplicate 
- Handled Missing values.

### Exploratory Data analysis
The exploration phase aimed to answer key questions such as...
- Who are the most dissatisfied and satisfied classes, and which services are they unhappy or happy with?
- How do Arrival and Departure times delay affect the satisfaction of passengers?
- What is the Age demographic of passengers?
- What is the likelihood of passengers recommending the airline?

### Data Analysis
- DAX codes used to find the NET PROMOTER SCORE
```DAX
  Promoters counts = CALCULATE(DISTINCTCOUNT('Unpivoted data'[ID]),FILTER('Unpivoted data','Unpivoted data'[Satisfaction]="Satisfied"))
  Detractor count = CALCULATE(DISTINCTCOUNT('Unpivoted data'[ID]),FILTER('Unpivoted data','Unpivoted data'[Satisfaction]="Neutral or Dissatisfied"))
  % promoters = DIVIDE( [Promoters counts],[Response Count])
  % Detractors = DIVIDE([Detractor count],[Response Count])
  Net Promoter Score = ( [% promoters]-[% Detractors])*100
```
### Results /Findings
Based on the analysis, 
- The airline's passenger satisfaction data reveals that 64% of unsatisfied clients are in Economy class, expressing significant dissatisfaction with cleanliness, ease of online booking, in-flight Wi-Fi, online boarding, and in-flight entertainment. In contrast, the majority of satisfied clients are in Business class, who appreciate online boarding, in-flight entertainment, baggage handling, in-flight services, and seat comfort. This disparity highlights the need for the airline to focus on improving the Economy class experience while maintaining the high standards valued by Business class travellers.
- Passenger dissatisfaction increases with longer arrival and departure delays.
- The airline's passenger demographic is predominantly composed of individuals in their 40s, who account for 30% of the total passenger count. This age group represents the largest segment of the airline's customer base.
- The airline's Net Promoter Score (NPS) stands at -13%, indicating that passengers are generally unwilling to recommend the airline to others. This negative score reflects significant dissatisfaction among customers and highlights the need for improvement in service and overall passenger experience.

 ### Recommendations 
 To improve the customer's satisfaction and overall experience,
 - it is recommended that the airline improve various services for the economy, with a particular emphasis on the following: Cleanliness, Ease of Online  booking, In-flight Wi-Fi services, Online Boarding and In-flight Entertainment.
 - The airline should prioritize improvements in Ease of Online booking and in-flight Wifi services, as these areas currently receive poor ratings and contribute to a negative overall Net Promoter Score (NPS). E Addressing issues with in-flight Wi-Fi, entertainment, and booking processes will significantly improve passenger satisfaction. By focusing on these critical aspects, the airline can boost its reputation and increase the likelihood of recommendations from travellers.

### Limitations 
A key limitation of our analysis is the presence of blank cells in the Arrival Delay and Departure Delay columns, which we could not fill. This lack of data may have affected the accuracy and reliability of our findings, hindering our understanding of the airline's on-time performance. Without this crucial information, we may have missed important insights related to delays and their impact on passenger satisfaction. Future analyses should prioritize obtaining complete datasets to enhance the robustness of our conclusions and recommendations.

### References 
- Stack Overflow
- youtube Analyze likert scale survey data [View here](https://youtu.be/H6g0im7sygI?si=93tMbqUvQziJKb5x)
- Youtube video sweatpants BI [View here](https://youtu.be/Uxr_ORnq0ys?si=Rb7bd1x808pJ7nnt)
  
  
