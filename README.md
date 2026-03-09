# Hospital-OPD-Analytics-Dashboard

<img width="345" height="286" alt="736b8580-2565-4e35-a4ea-df390c849c7e" src="https://github.com/user-attachments/assets/dc3325ae-73e7-4a04-920f-8388f4472fcd" />


<details>
<summary id="introduction"> Introduction</summary>


A healthcare analytics dashboard built with Power BI to analyze outpatient department (OPD) attendance, patient retention, visit frequency, and demographic trends.



To support data-driven decision-making in hospital management, the dashboard seeks to answer several key business questions related to patient demand, demographics, retention, and operational efficiency.

- What are the overall trends in outpatient department (OPD) patient attendance over time?

- What demographic groups (age, gender, and location) represent the majority of patients visiting the hospital?

- What proportion of patients are new versus returning, and how frequently do patients revisit the hospital?

- When does the hospital experience the highest patient demand in terms of days and hours of operation?

  

The primary objective of this dashboard is to provide actionable insights into outpatient department (OPD) activity by analyzing patient attendance, demographics, visit patterns, and operational demand to support data-driven decision-making in healthcare management.


To achieve this goal, the dashboard focuses on several key analytical areas that provide a comprehensive understanding of outpatient department performance and patient behavior:

- Monitor outpatient department (OPD) patient attendance and demand trends;

- Analyze patient demographics to understand the hospital's service population;

- Evaluate patient acquisition and retention patterns;

- Identify peak operational hours to optimize hospital resource allocation;

- Assess patient visit frequency to understand healthcare utilization patterns;

</details>

---

<details>
<summary id="etl-process"> ETL Process</summary>


The analysis followed a structured **ETL pipeline**:


### - Data Extraction

* Connected Power BI to the hospital database (Excel / CSV)
  

### - Data Cleaning

* Handled missing values using complete case analysis for critical fields (`Patient_ID`, `Date`, `Age`, `Gender`)
* Filled non-critical missing values (`Payment_Type` & 'Location') with default values (e.g. 'Unknown')
* Corrected inconsistent values (e.g., negative ages, impossible timestamps in `Time_In`/`Time_Out`)
* Standardized categorical values (`Gender`: Male/Female, `Payment_Type`: Private/Insurance/Other)


### - Data Transformation

* Created additional calculated columns: Age_Group, Cohort_Month, First_Visit_Date, Hospital_Rush
  
* Built supporting tables for temporal and demographic analysis (Daily Visits, Monthly Cohorts, Payment Trends)

---

### - Measures & KPIs

Create measures and KPIs: Average Age, Average Days Between Visits, Average Visits per Day, New Patient Acquisition Rate, Total Patients, Retention Rate & Peak Hours/Hospital Rush.

</details>

---
<details>

<summary id="dashboard-overview">Dashboard Overview</summary>


###  Demographics  and patient visits patterns Dashboard

<img width="867" height="488" alt="image" src="https://github.com/user-attachments/assets/0572312e-3cae-43b2-96db-1d3aeb0bb47b" />


###  Temporal and cohort analysis Dashboard
<img width="876" height="494" alt="image" src="https://github.com/user-attachments/assets/7897b7fd-5883-4efd-952d-489e89567062" />

</details>

---
<details>

<summary id="results--insights"> Results / Insights</summary>



Here’s a polished storytelling-style insight summary for your OPD Attendance Dashboard, fully integrating the detailed points you provided:


### **The Story of Our Hospital’s Patient Flow and Performance**

Step inside our hospital, and you’ll see a vibrant ecosystem of care. Every year, **12,000 patients** seek our services, with an **average of 72 patients per day**. This steady flow reflects a **6.1% growth rate**, showing that our hospital continues to attract new individuals while retaining loyal visitors. In fact, **55% of our patients are new**, while **45% are returning**, highlighting both our outreach success and patient trust.

#### **1. When and How Patients Visit**

* **Morning Rush:** The busiest window is the morning, with **7.1K visits**, followed by afternoons, evenings, and nights.
Peak days are **Mondays and Tuesdays**, particularly in the morning shift. This insight is crucial for optimizing staff allocation and reducing wait times.
* **Outpatient Focus:** A striking **88% of our volume is outpatient care**, confirming that our hospital primarily serves as a primary care and diagnostic center.

#### **2. Patient Loyalty and Retention**

* Our **retention rate of 75.5%** is a strong testament to patient satisfaction and trust.
* Most patients visit **once (6.4K)**, but a significant portion comes **2–4+ times**, reflecting chronic care needs or scheduled follow-ups.
* With an **average interval of 47 days between visits**, our patient cohorts—especially older ones—demonstrate long-term engagement.

#### **3. Who Are Our Patients?**

* **Age Distribution:** Young adults dominate, with **18–35 years old (4.4K)** forming the largest group, followed by **36–50 years**. Pediatrics and seniors make up smaller portions.
* **Gender Balance:** A slight majority are male (**54%**) versus female (**46%**), suggesting a fairly balanced patient population.
* **Payment Trends:** Private pay (**5.6K**) and insurance (**3.9K**) lead our revenue streams, signaling strong financial stability and preference for premium services.

</details>

---
<details>

<summary id="recommendations"> Recommendations</summary>


**Based on the insights, the following strategic actions are recommended:**


### **1. Optimize Staffing and Operational Efficiency**

* **Morning & Early-Week Focus:** Increase staffing during **morning shifts**, especially on **Mondays and Tuesdays**, to handle peak patient volumes and reduce wait times.
* **Flexible Scheduling:** Implement dynamic staffing or shift rotations aligned with **hourly patient flow** to maximize efficiency without overstaffing during quieter periods (evenings and nights).
* **Outpatient Prioritization:** Given that **88% of patients are OPD**, consider separate streams or dedicated zones for outpatient care to improve patient flow and reduce congestion.


### **2. Enhance Patient Retention and Engagement**

* **Follow-Up Reminders:** With an **average of 47 days between visits**, implement automated follow-up reminders (SMS/email) for returning patients, particularly those with chronic care needs.
* **Loyalty Programs:** Develop targeted programs for returning patients (45% of total), such as priority appointments or health packages, to maintain and improve the **75.5% retention rate**.
* **Segmented Care Plans:** Identify frequent visitors (2–4+ visits) and provide tailored care or preventive programs to reduce unnecessary repeat visits while enhancing patient satisfaction.


### **3. Targeted Outreach for Growth**

* **New Patient Acquisition:** Since **55% of patients are new**, continue marketing and community outreach programs focusing on younger adults (18–35 years) who make up the largest demographic.
* **Patient Education:** Provide health awareness campaigns or wellness programs to attract and retain younger patients while educating them on preventive care.


### **4. Financial and Service Strategy**

* **Private & Insurance Pay Focus:** Since **private pay (5.6K) and insurance (3.9K)** dominate revenue, introduce **premium service packages** or expand insurance partnerships to improve financial stability.
* **Payment Flexibility:** Offer convenient payment options for mid-tier and self-pay patients (3K) to enhance accessibility and encourage repeat visits.



### **5. Data-Driven Continuous Improvement**

* **Monitor Peak Trends:** Regularly track daily and hourly patient patterns to adjust staffing, appointment slots, and resource allocation in real time.
* **Cohort Analysis:** Analyze returning patient cohorts to understand long-term engagement trends and anticipate resource needs for chronic care or specialized services.
* **Dashboard Updates:** Keep your OPD dashboard current with real-time data to support ongoing operational decisions and strategic planning.

</details>

---

[![Power BI Dashboard](https://img.shields.io/badge/Click_here_to_access_the_interactive_dashboard-F2C811?style=for-the-badge&logo=microsoftpowerbi&logoColor=black)](https://app.powerbi.com/view?r=eyJrIjoiZDU0YTIwNTEtN2VjMi00NjA5LWJkOTgtOTI2MGQwMDIyY2RmIiwidCI6Ijk0MWJiZjVmLWYyYzAtNDg3NS1hMjRjLTY5MDc4NjVkMjUxYSIsImMiOjh9)




## 🔗 Connect with me

For questions or collaborations, feel free to reach out!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/koko-mukuru-yves-98621a14a) 
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kokomukuruy@gmail.com)

---
<p align="center">
  <i>"Turning data into actionable insights, one project at a time."</i>
</p>

**© 2026 Koko Mukuru Yves**. All rights reserved






