# OMS 2.0 Enhancement Dashboard  

## **Project Background**  
RICOH is a leading **digital printing and imaging solutions provider**, operating in the print and document management industry for over **30 years**. The company’s business model revolves around providing **hardware, software, and managed services** to enterprise clients worldwide.  

The **OMS 2.0 Enhancement and Migration Project** was initiated as part of RICOH’s ongoing commitment to improving **user experience (UX)** and **system integration**. The goal was to modernize and unify printer login methods and user interfaces across the **client’s global printer fleet** — encompassing **6,000+ devices** across **15+ office locations**.  

As a **data analyst** on this project, my role was to design and maintain a **dashboard** that provides real-time **reporting and tracking** for project stakeholders, including project managers and client representatives. The dashboard was built to:  
- Monitor the **enhancement process** and **implementation timeline**  
- Observe **daily trends** in device migration success and failure  
- Track the **overall progress** and identify **bottlenecks** for timely resolution  

### **Data Tools & Technologies Used**
- **SharePoint** → Primary data source (updated daily by Asset and Project Managers)  
- **Power Query** → Data extraction and cleaning  
- **DAX (Data Analysis Expressions)** → Custom measures and calculated fields  
- **Power BI Desktop** → Interactive dashboard development  
- **Power BI Service** → Online publishing with **daily automatic data refresh**  

---

## **Data Structure & Initial Checks**  
The main data source for the project was **SharePoint**, maintained daily by the Asset and Project Managers. Each printer’s enhancement status was tracked against the master **Asset List**, using fields such as:  
- `To be migrated? (Y/N)`  
- `Migrated successfully? (Y/N)`  
- `Reason of failure`  

Daily project meetings were held at **12:00 PM** to review progress, identify issues, and plan next steps.  

### **Database Overview**
The dataset contained approximately **3,000 records** representing individual printer assets, structured across four tables:  

| **Table** | **Description** |
|------------|----------------|
| **Table 1 – Asset List** | Contains all devices under the global account’s fleet, with device identifiers and location details. |
| **Table 2 – Migration Status** | Tracks the migration progress of each device (`To be migrated`, `Migrated successfully`, etc.). |
| **Table 3 – Failure Logs** | Logs migration errors and their causes (`Offline`, `Not in System`, `Network Error`). |
| **Table 4 – Project Timeline** | Daily updates including migration phase, progress percentage, and project notes. |

[![Entity Relationship Diagram Placeholder](# "Entity Relationship Diagram")](#)

---

## **Executive Summary**

### **Overview of Findings**
Over the course of **19 weeks**, the OMS 2.0 migration project achieved a **99.24% successful migration rate** across the targeted printer fleet.  
The main challenges were **offline or unregistered devices**, requiring follow-up with local IT teams. Despite these issues, the project reached completion **on time and within scope**.  

### **Key Takeaways for Stakeholders (e.g., Project Manager)**
1. **99.24%** of devices were successfully migrated within the planned 19-week period.  
2. Primary causes of migration failure were **logistical (offline/unregistered)** rather than technical.  
3. The Power BI dashboard enabled **real-time visibility**, improving coordination between regional and central teams.  

!(https://github.com/NTNM-Nguyen/oms2-migration-dashboard/blob/main/Screenshot%202025-10-14%20202131.png)


---

## **Insights Deep Dive**

### **Category 1: Summarized Data**
A set of **card visuals** provides a snapshot of key performance metrics:
- Total devices in migration scope  
- Total attempted migrations  
- Successful vs. failed migrations  
- Current week’s progress  

These summary cards give stakeholders a **quick project health check** during daily meetings.

[![Summary Metrics Visualization](# "Summary Data Cards")](#)

---

### **Category 2: Trend Analysis**
Three **trend visuals** were developed to show performance over time:
1. **Weekly successful vs. remaining devices**  
2. **Weekly successful vs. failed devices**  
3. **Cumulative migration success vs. failure rates**  

These visuals helped identify weekly progress trends and highlighted performance dips during **holiday periods** and a **planned one-week break**.

[![Trend Analysis Visualization](# "Weekly and Cumulative Trends")](#)

---

### **Category 3: Failed Devices and Reasons**
A **pie chart visualization** illustrates the top causes of failed migrations:
- **Offline Devices** (most frequent issue)  
- **Devices not listed in the client’s system**  
- **Network accessibility issues**  

This breakdown allowed the team to **prioritize troubleshooting efforts** and communicate with local site managers for resolution.

[![Failure Reason Distribution Chart](# "Reasons for Failed Migrations")](#)

---

## **Recommendations**

1. **Improve Migration Speed**  
   - Introduce predictive scheduling to flag and prioritize at-risk devices.  

2. **Reduce Migration Errors**  
   - Implement automated pre-check scripts to validate device connectivity and registration prior to migration.  

3. **Enhance Data Governance**  
   - Maintain consistent SharePoint data formatting and enforce data entry validation rules.  

4. **Scalability & Reuse**  
   - The Power BI tracking framework can be **replicated for other migration projects** or **adapted for global accounts** with similar requirements.  

---

## **Assumptions and Caveats**
- The **SharePoint Asset List** was assumed to be complete and up to date.  
- **External factors** (e.g., holidays and a one-week project pause) were excluded from migration efficiency KPIs.  
- The **database structure** was maintained consistently by Asset and Project Managers throughout the project.  

---

*Authored by: Minh Nguyen — Business Intelligence Developer*  
*Linkedin: www.linkedin.com/in/minh-n-nguyen*
