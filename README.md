# OMS 2.0 Enhancement Project Tracker  

## **Project Background**  
RICOH is a leading **digital printing and imaging solutions provider**, operating in the print and document management industry for over 88 years. The company’s business model revolves around providing **hardware, software, and managed services** to enterprise clients worldwide.  

The **OMS 2.0 Enhancement and Migration Project** was initiated as part of RICOH’s ongoing commitment to improving **user experience (UX)** and **system integration**. The goal was to modernize and unify printer login methods and user interfaces across a major client’s global printer fleet — encompassing **5,000+ devices** across **20+ country locations**.  

As a **Business Intelligence developer**, I partnered with the project team to design a dashboard solution that provides **reporting and tracking** for project stakeholders, including project managers and client representatives. The dashboard was built to:  
- Monitor the **enhancement process** and **implementation timeline**  
- Observe **weekly trends** in migration success/failure, showcase **migrated vs. remaining devices to date** compared to the whole fleet 
- Track the **overall progress** and identify **bottlenecks** for timely resolution

⏰The solution also to be scheduled for automatic refresh in time for daily project meetings held at *12:00 PM* to review progress, identify issues, and plan next steps.  

 Week 7             | Week 19  
:-------------------------:|:-------------------------:
 ![](Assets/Screenshot_2025-10-14_202640.png) | ![](/Assets/Screenshot_2025-10-14_202131.png) 

### **Data Tools**
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

---

## **Executive Summary**

### **Overview of Findings**
Over the course of 19 weeks, the OMS 2.0 migration project achieved a **99.24% successful migration rate** across the targeted printer fleet. The most significant jump in attempted and sucessful device happened after week 10 (week 41 calendar year), from 83 to 792 sucessful enhancement (~854% ⬆️increase), we can see 72% of the project was done within the last 7 weeks due to offices back from summer holiday, established processes, and increase in communication and cross-function synergies. The majority 77% of the client's fleet is located in EMEA region which is also the region with the highest failed migrations, the main challenges were **offline or unregistered devices**, requiring follow-up with local IT teams rather than technical.

---

## **Insights Deep Dive**

### **Project Snapshot**
A combined **card visuals** provides a snapshot of key performance metrics:
- Total devices in migration scope  
- Total attempted migrations  
- Successful vs. failed migrations  
- Current week’s progress
These summaries give stakeholders a **quick project health check** during daily meetings without the need of locating and trying to read the data from different visuals.
<img width="462" height="217" alt="Screenshot 2025-10-17 210448" src="https://github.com/user-attachments/assets/8e16be9b-c25b-4333-93ea-b11570c952f5" />

---

### **Enhancement Trend**
- The project began with a slow ramp-up phase, with only 18 successful migrations in the first three weeks.
- A sharp increase occurred starting Week 35 (555 devices) through Week 42 (2,256 devices) — reflecting full operational deployment and stabilized migration processes.
- Migration speed was highest between Weeks 42 and 45, adding roughly 1,500+ devices per week.
- By Week 43, cumulative success reached 3,335 devices, suggesting the team had achieved over 60% completion of the total target fleet.
  
 Successful vs. remaining devices             | Weekly and Accumulated Status
:-------------------------:|:-------------------------:
<img width="546" height="380" alt="Trend 1" src="https://github.com/user-attachments/assets/76edd3af-c2ba-47ce-be9c-21f2c0a551ee" /> | <img width="905" height="380" alt="trend 2" src="https://github.com/user-attachments/assets/8dd14680-0a8e-48de-8f67-85b10f2268fe" />
---

### **Failed Devices and Reasons**
- EMEA region accounted for 77% of the total fleet with 4250 attempted devices, this region also has the highest number of unsuccessful devices of 55 (1.2% error rate). APAC, NAM, LATAM region all achieve high sucessful migration rate from 99% - 100%.
- The most common reasons of failure are *Device offline* (38% - 21 devices), Devices not registered in online system SLNX (32& - 18 devices), Devices in storage (29% - 16 devices). All requires addional clarification with client's local offices which adds to project's execution timeline.
- This breakdown allowed the team to **prioritize troubleshooting efforts** and communicate with local site managers for resolution.
  
 Reason of failure             | Migration Status by Region
:-------------------------:|:-------------------------:
<img width="329" height="271" alt="pie" src="https://github.com/user-attachments/assets/e41ad501-e300-425f-8659-f192677283ca" /> | <img width="320" height="271" alt="Screenshot 2025-10-17 210509" src="https://github.com/user-attachments/assets/1219236f-39ad-4688-a70b-c1cdca898663" />

---

## **Recommendations**
**Improve Migration Speed**  
   - The early slow weeks likely involved procedural setup, user access, and configuration testing. Create a standardized onboarding checklist to reduce lead time in future migrations.
   - The middle phase achieved the best throughput and lowest error rates. Capture key factors (e.g., staff allocation, communication cadence, device pre-check scripts) and formalize them into a scalable migration playbook for future global accounts.
**Reduce Migration Errors**  
   - Implement automated pre-check scripts to validate device connectivity and registration prior to migration. Cut time spend on locating offline devices and waiting for response.
**Enhance Data Governance**  
   - Maintain consistent SharePoint data formatting and enforce data entry validation rules. Ensure mandatory columns remain unchanged and correctly filled in.

---

## **Assumptions and Caveats**
- The **SharePoint Asset List** was assumed to be complete and up to date.  
- **External factors** (e.g., holidays and a one-week project pause) were excluded from migration efficiency KPIs.  
- The **database structure** was maintained consistently by Asset and Project Managers throughout the project.  

---

*Authored by: Minh Nguyen — Business Intelligence Developer, Data Analyst*  
*Linkedin: www.linkedin.com/in/minh-n-nguyen*
