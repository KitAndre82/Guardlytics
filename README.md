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


### Data Dictionary
**File: guard_shift_schedule_with_weekly_hours.csv**
#### Column	                   
- Guard_ID:	                 Unique identifier for each guard
- Date:	                     Date of the shift
- Week:	                     Week number of the year
- Regular_Shift:             Scheduled shift for the guard (Morning, Afternoon, Night)
- Actual_Shift:	             Actual shift worked by the guard
- Is_Covering:               Boolean indicating if the guard is covering for someone else
- Site:	                     Name of the site (e.g., Oakland, Los Angeles)
- Clock_In:	                 Actual clock-in timestamp
- Clock_Out:                 Actual clock-out timestamp
- Hours_Worked:	             Total hours worked in that shift
- Weekly_Hours:	             Cumulative hours worked in the week
- Over_40_Hours:             Boolean indicating if weekly hours exceeded 40

**File: synced_guard_patrols.csv**
#### Column	                   
- Timestamp:	               Timestamp when the patrol or scan was recorded
- Site:	                     Site where the patrol occurred
- Guard_ID:	                 Unique identifier of the guard
- Shift:	                   Shift during which the patrol was conducted (Morning, Afternoon, Night)
- Interior_Exterior:	       Indicates whether the patrol was interior or exterior
- Incident_Type:	           Type of security incident (e.g., Theft, Disturbance, Unauthorized Access)
- Response_Time_Minutes:	   Time taken to respond to the incident, in minutes
- Patrol_Completed:	         Boolean flag indicating whether the patrol was completed
- QR_Scans:	                 Number of QR code scans performed during the patrol
- QR_Code_Locations_Scanned: List of QR scan locations visited during the patrol
- Overtime_Hours:	           Overtime hours accrued during this patrol
- Week:	                     Week number of the patrol
- Month:	                   Month in which the patrol occurred (added in preprocessing)
- Day:	                     Day of the week for the patrol (added in preprocessing)

