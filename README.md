🕵️‍♀️ Crime in India Dashboard (2020–2024)
Prepared by: Shrawani Gongshe
Tool Used: Power BI

📊 Overview
A comprehensive Power BI dashboard analyzing crime statistics across India from 2020 to 2024.

🔍 Objective
To analyze and visualize key crime trends and statistics to enable better policy and enforcement strategies.

📌 Key Metrics
Total Crimes: 40K

Closed Cases: 20K

Unresolved Rate: 0.50

📐 DAX Measures Used
dax
Copy
Edit
Total Crimes = COUNT('crime_dataset_india'[Report Number])

Closed Cases = CALCULATE(
    COUNT('crime_dataset_india'[Report Number]), 
    'crime_dataset_india'[Case Closed] = "Yes"
)

Unresolved Cases = CALCULATE(
    COUNT('crime_dataset_india'[Report Number]),
    'crime_dataset_india'[Case Closed] = "No"
)

Unresolved Rate (%) = DIVIDE([Unresolved Cases], [Total Crimes], 0)
These measures drive the core KPIs and help visualize overall crime load, resolution efficiency, and open cases.

🏙️ Crimes by City
Top cities with the highest crime rates:

Delhi

Mumbai

Bangalore

Insight: Metropolitan areas like Delhi have the highest reported crimes.

📅 Crimes by Day of the Week
Insight: Higher incidents occur on:

Thursday

Wednesday

Sunday

Use Case: Optimize police deployment on peak days.

⏰ Crimes by Hour of the Day
Insight: Most crimes occur between 6 PM – 12 AM.

Implication: Heightened police alertness is needed during evening hours.

⚠️ Crimes by Severity
Severity Categories:

Extreme

High

Medium

Low

Other

Insight: Most crimes fall under Medium to High severity.

👥 Crimes by Age Group
Age Groups:

Adults

Young Adults

Juveniles

Elderly

Insight: Adults and Young Adults are the largest victim groups.

🚻 Crimes by Victim Gender
Genders:

Male

Female

Other

Insight: Males are more frequent victims, but crimes against females are significantly high.

🌗 Crimes by Shift
Shifts Analyzed:

Morning

Afternoon

Evening

Night

Insight: Afternoon and Evening shifts see the highest crime rates.

🧭 Crimes by Domain
Crime Domains:

Violent Crime

Fire Accident

Traffic Fatality

Other

Insight: Violent and traffic-related crimes dominate.

📍 State-wise Crime Summary
Example Stats:

Maharashtra: 8046 total crimes

Delhi: 5400 total crimes

Average closure rate: ~50% across states

📝 Crimes by Description
Top Crime Types:

Burglary

Robbery

Assault

Cybercrime

Insight: Urban and digital crimes are notably prevalent.

🗺️ Map of Crimes by Domain
Insight: Visual map showing hotspots for domains like violent crimes and traffic fatalities.

✔️ Recommendations
Increase surveillance during peak crime hours

Prioritize high-crime cities

Improve case closure rates

Launch gender and age-targeted safety programs

🧾 Conclusion
Crime trends in India vary by city, time, and demographic. Power BI enables actionable insights that can inform effective crime prevention and resolution strategies.
