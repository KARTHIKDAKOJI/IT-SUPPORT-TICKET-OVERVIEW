# IT-SUPPORT-TICKET-OVERVIEW
![Alt text](https://github.com/KARTHIKDAKOJI/IT-SUPPORT-TICKET-OVERVIEW/blob/a96cbbbca0b42c0a83426158331c4b4517aabc2d/support_ticket_f20%20challenege_page-0001.jpg)


This project was made as part of the FP20 Analytics Challenge 28. The main goal was to analyze and visualize IT support ticket data using Power BI. The dashboard helps us understand how tickets are handled, how long they take to resolve, and where there are delays or problems.






# 📊 Summary of Key Numbers
Metric	Value

Total Tickets	11,923

Average Tickets Per Day	23

Average Resolution Time	2.82 days

High Priority Tickets	4,571 (38%)

These numbers show a busy support team with many high-priority issues.

# 📅 Monthly Ticket Trends
❄️ February (2024 & 2025) had fewer tickets — possibly due to holidays or less activity

💪 March showed a strong comeback both years

📉 April to September 2024 stayed steady

❗ June 2025 had 0 tickets, which likely means data is missing or broken

👉 What to do: Set up checks to catch missing data early.

# 📂 Support Queues & Priorities
Technical Support and Product Support teams handled the most tickets

⚠️ A high number of tickets (38%) were marked as “High Priority” — this seems too much

🕒 General Enquiry and HR tickets took the longest to resolve

👉 Suggestions:

Use automatic rules to decide what really needs “high priority”

Add chatbots or FAQs for common questions

Train teams to help each other across departments

# 🏷️ Ticket Tags and Delays
Most used tags: Security, Feedback, Technical, Performance

Tags with longest delays:

Feedback: 2.89 days

Documentation and Performance: also slow

👉 Suggestions:

Use tags consistently across all tickets

Create standard processes for tags that often cause delays

Improve internal guides and documentation

# 🌍 Country-wise Insights
Country	Tickets	Avg. Resolution Time
Belgium	1,240	2.83 days
Sweden	1,238	2.80 days
Latvia	1,232	2.80 days
Poland	1,180	2.85 days (slowest)

Belgium, Sweden, and Latvia got the most tickets. Poland had slightly slower response times.

👉 Suggestions:

Give more help to teams in countries with high load

Train teams in slower countries to improve speed

Share knowledge better between teams

# ✅ Measures  To be Taken
Fix high-priority misuse — Use rules and automation

Check missing data — Run regular audits

Clean up ticket tags — Use a standard format

Train slower teams — Offer toolkits and workshops

Track slow categories — Focus on tags with delays

Plan better — Use monthly data to schedule team capacity

# charts
| Chart Name               |  Type of Chart    |                  Why It Was Used                   |
| ------------------------ | ----------------- | -------------------------------------------------- |
| Overview Cards           | KPI Cards         | Show total tickets, daily average, resolution time |
| Monthly Ticket Trend     | Line Chart        | Show ups and downs across months                   |
| Queue vs Resolution Time | Bar Chart         | Compare which team/queue takes longer              |
| Tag Volume & Delay       | Bar + Table       | Find common tags and how long they take to resolve |
| Country-wise Load & Time | Map + Table       | Show how countries compare in volume and time      |
| Ticket Type & Tag Delay  | Matrix Table      | See delay based on ticket type and tag             |



# DAX formulas used
1. avg_resoltime = AVERAGE(Table1[resolution_time])

2. avg_tickets/day = DIVIDE(COUNT(Table1[Ticket ID]), DISTINCTCOUNT(Table1[Date]), 0)

3. m-o-m = CALCULATE(COUNT(Table1[Ticket ID]), DATEADD(calender[Date].[Date], -1, MONTH))

4. m-o-m (%) = DIVIDE(Table1[total tickets] - [m-o-m], [m-o-m], 0)

5. priority_high = CALCULATE(COUNT(Table1[Priority]), Table1[Priority] = "high")

6. total tickets = COUNT(Table1[Ticket ID])





# 🛠 Tools Used
Power BI — To create charts and dashboards

DAX — To calculate averages and custom measures

ZoomCharts — For interactive visuals

PDF/Excel — As the main data sources

