# OMS 2.0 Enhancement Project Tracker  

## **Project Background**  
RICOH is a leading **digital printing and imaging solutions provider**, operating in the print and document management industry for over 88 years. The company’s business model revolves around providing **hardware, software, and managed services** to enterprise clients worldwide.  

The **OMS 2.0 Enhancement and Migration Project** was initiated as part of RICOH’s ongoing commitment to improving **user experience (UX)** and **system integration**. The goal was to modernize and unify printer login methods and user interfaces across a major client’s global printer fleet — encompassing **6,000+ devices** across **15+ office locations**.  

As a **Business Intelligence developer**, I partnered with the project team to design a dashboard solution that provides **reporting and tracking** for project stakeholders, including project managers and client representatives. The dashboard was built to:  
- Monitor the **enhancement process** and **implementation timeline**  
- Observe **weekly trends** in migration success/failure, showcase **migrated vs. remaining devices to date** compared to the whole fleet 
- Track the **overall progress** and identify **bottlenecks** for timely resolution

⏰The solution also to be scheduled for automatic refresh in time for daily project meetings held at *12:00 PM* to review progress, identify issues, and plan next steps.  

![Dashboard Overview](/Assets/Screenshot_2025-10-14_202131.png)

### **Data Tools & Technologies Used**
- **SharePoint** → Primary data source 
- **Power Query** → Data extraction and cleaning  
- **DAX (Data Analysis Expressions)** → Custom measures and calculated fields  
- **Power BI Desktop** → Interactive dashboard development  
- **Power BI Service** → Online publishing with **daily automatic data refresh**  

---

### **Database Overview**
The main data source for the project was **SharePoint**, maintained daily by the Asset and Project Manager. Each printer’s enhancement status was tracked against the master **Asset List**. The dataset contained approximately **6,000 records** representing individual printer devices, consisted of three parts:  

| **Table Section** | **Description** |
|------------|----------------|
| **Asset List** | Contains all devices under the global account’s fleet, with device identifiers and location details. |
| **Migration Status** | Tracks the migration progress of each device (`To be migrated`, `Migrated successfully`, `Mirgration time` etc.). |
| **Failure Logs** | Logs migration errors and their causes (`Offline`, `Not in System`, `Network Error`). |

<img width="1812" height="852" alt="Screenshot 2025-10-17 121026" src="https://github.com/user-attachments/assets/e303f10c-9b82-4df6-b11c-f16a4c8b25db" />
<img width="752" height="337" alt="Screenshot 2025-10-17 144558" src="https://github.com/user-attachments/assets/bcaddf7a-25b3-4c4a-bae3-9e8829f351ec" />

---

## **Executive Summary**

### **Overview of Findings**
Over the course of 19 weeks, the OMS 2.0 migration project achieved a **99.24% successful migration rate** across the targeted printer fleet.  
The main challenges were **offline or unregistered devices**, requiring follow-up with local IT teams. Despite these issues, the project reached completion on time and within scope thanked to the close collaboration and effort from both RICOH and client teams.

### **Key Takeaway**
1. **99.24%** of devices were successfully migrated within the planned 19-week period.  
2. Primary causes of migration failure were **logistical (offline/unregistered)** rather than technical.  
3. The most significant jump in attempted and sucessful device happened after week 10 (week 41 calendar year), from 83 to 792 sucessful enhancement (~854% ⬆️increase), we can see 73% of the project was done within the last 7 weeks due to increase in communication and teams working together

---

## **Insights Deep Dive**

### **Project's current status and Snapshot**
A set of **card visuals** provides a snapshot of key performance metrics:
- Total devices in migration scope  
- Total attempted migrations  
- Successful vs. failed migrations  
- Current week’s progress  

These summary cards give stakeholders a **quick project health check** during daily meetings.

[![Summary Metrics Visualization](# "Summary Data Cards")](#)

---

### **Enhancement Trend**
Three **trend visuals** were developed to show performance over time:
1. **Weekly successful vs. remaining devices**  
2. **Weekly successful vs. failed devices**  
3. **Cumulative migration success vs. failure rates**  

These visuals helped identify weekly progress trends and highlighted performance dips during **holiday periods** and a **planned one-week break**.

[![Trend Analysis Visualization](# "Weekly and Cumulative Trends")](#)

---

### **Failed Devices and Reasons**
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
