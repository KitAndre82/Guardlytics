# Guardlytics
This project analyzes guard scheduling, patrol activity, incident response, and shift performance using real-world-style data from a private security company. Built with Python and Seaborn/Matplotlib, it uncovers patterns in guard punctuality, patrol completion rates, response times, and incident trends across multiple sites and shifts.

#  Guardlytics: Data-Driven Security Operations Analysis

##  Overview

**Guardlytics** is a comprehensive data analytics project focused on evaluating security guard performance, patrol activity, and incident response across multiple sites and shifts for a private security company. Using Python and visualization libraries like Seaborn and Matplotlib, the project extracts operational insights from scheduling and patrol datasets to support decision-making, staffing optimization, and resource allocation.

---

##  Objectives

- Monitor guard attendance, shift punctuality, and shift coverage
- Evaluate patrol completion rates and QR location scans
- Analyze incident frequency and response times by guard, shift, and location
- Identify performance trends to support operational improvements
- Provide visual insights into workload distribution and inefficiencies

---

##  Key Insights

- **Guard Lateness**: Certain guards (e.g., Guard 1001, Guard 1091) were frequently late, especially during morning and night shifts.
- **Coverage Dependence**: Guards 1026 and 1057 covered over 30 shifts each — highlighting workload imbalance.
- **Patrol Completion**: Average completion was high, but some guards missed >4% of assigned patrols.
- **Incident Trends**: Most incidents occurred during morning shifts; theft and unauthorized access were most common.
- **Response Time**: Best performers responded in ~11.3 mins; worst exceeded 13 mins.
- **QR Location Activity**: Interior areas like Control Room and Server Room had the most QR scans — signaling effective coverage.
- **Overtime Usage**: Morning shifts had the highest overtime, pointing to potential understaffing or scheduling inefficiencies.

---

##  Data Sources

- `guard_shift_schedule_with_weekly_hours.csv` – Contains clock-in/out data, shifts, hours worked, and coverage flags.
- `synced_guard_patrols.csv` – Contains patrols, incidents, QR scans, response times, and location metadata.

---

##  Analysis Highlights

- Attendance and lateness patterns by shift and guard
- Patrol completion rates by guard and location
- Incident response time benchmarking
- Incidents by QR scan location and shift
- Overtime analysis by shift
- Monthly and site-level patrol volume distribution

Visualizations are provided to easily interpret trends and identify high-risk shifts or guards requiring attention.

---

##  Tools & Technologies

- **Python 3.11+**
- **Pandas** for data manipulation
- **NumPy** for numerical calculations
- **Seaborn & Matplotlib** for data visualization
- **Datetime** for time-based features
- **Jupyter Notebook** for exploratory analysis


   git clone https://github.com/your-username/guardlytics-security-analysis.git
   cd guardlytics-security-analysis
