# **Airline Operations Intelligence: Engineering Log & System Architecture**

**Executive Summary**
This repository documents the engineering of a secure, enterprise-grade data ecosystem for the aviation sector. Moving beyond static reporting, this project focuses on the **Technical Integrity** of the data lifecycle—implementing multi-source ETL pipelines, high-performance relational modeling, and DAX-driven security protocols to support real-time operational decision-making.

---

## **System Demonstration**
**[Technical Walkthrough & Video Link]** — [https://drive.google.com/drive/folders/1RAXYOuvcT-ATD2552MjY-](https://drive.google.com/drive/folders/1RAXYOuvcT-ATD2552MjY-)

---

## **The Tech Stack**
* **Analytics Engine:** Power BI Desktop / Power BI Service
* **ETL Framework:** Power Query (M Language)
* **Data Modeling:** Star-Schema Relational Mapping
* **Security Layer:** Row-Level Security (RLS) & On-Premises Data Gateways

---

## **Module I: The Data Pipeline: ETL & Transformation Log**

The ingestion phase involved harmonizing three primary data streams: **Flights**, **Passengers**, and **Tickets**.

* **Power Query Logic:** Implemented advanced data sculpting using M-logic to standardize disparate time-series data and handle null-value propagation across the `FlightID` primary key. 
* **Feature Engineering:** Programmatically extracted numeric identifiers from alphanumeric flight strings to optimize indexing and visualization clarity. Integrated conditional performance classification to allow for rapid identification of "Best" vs. "To Be Improved" routes.

---

[Power Query Applied Steps & ETL Logic]<img width="1435" height="751" alt="image" src="https://github.com/user-attachments/assets/91165973-491f-4dbe-b9e5-7fbe11957357" />


---

## **Module II: Schema & Relational Logic**

A high-performance **Star Schema** was developed to ensure low-latency cross-filtering and data consistency across the multi-page report environment.

* **Architecture:** Centered on a 1:Many relational model, using `FlightID` as the primary join key between operational flight schedules, transactional ticket data, and passenger demographics.
* **Integrity Management:** Configured precise cross-filter directions and cardinality to prevent ambiguous relationships, ensuring metrics remain accurate during granular drill-downs.

---

[Star Schema and Relational Model View]<img width="1439" height="708" alt="image" src="https://github.com/user-attachments/assets/6b031d84-b872-48dc-9eec-fa17636e5482" />


---

## **Module III: Security Infrastructure & Governance**

This project is built for secure enterprise deployment, emphasizing data privacy and automated lifecycle management.

* **Row-Level Security (RLS):** Engineered DAX-based roles to enforce jurisdiction-based access. This ensures that sensitive passenger and financial data is only visible to authorized regional stakeholders.
* **Automation:** Configured **Scheduled Refreshes** via the Power BI Service, maintaining the "Truth" of the data through automated gateway updates that occur daily without manual intervention.

---

[Security Roles and Refresh Configuration]<img width="634" height="343" alt="image" src="https://github.com/user-attachments/assets/3cef6fd5-7e86-43c6-b3ef-2d2281542d22" />




---

## **Module IV: Analytical Verdict: Final Dashboard Interface**

The engineering efforts culminate in a high-fidelity operational interface that tracks route efficiency, passenger load factors, and booking trends in real-time.

| Analytical Question | Technical Solution | Operational Result |
| :--- | :--- | :--- |
| **Which routes are underperforming?** | Conditional Logic Classification | Immediate identification of flights requiring review. |
| **Where is the passenger surge?** | Multi-variate Geographic Mapping | Optimized resource allocation at high-traffic hubs. |
| **Is data access secure?** | DAX Row-Level Security (RLS) | Mitigation of data privacy risks for sensitive info. |
| **Is the data current?** | Scheduled Refresh Pipelines | Automated daily updates for dynamic pricing monitoring. |

---

[Operational Intelligence Dashboard]<img width="1438" height="728" alt="image" src="https://github.com/user-attachments/assets/dcac7741-810b-490a-a223-be8a695e1e9d" />


*Caption: The centralized dashboard provides a unified telemetry view of the airline’s operational health.*

---

## **Technical Repository Map**
* **`data/`**: Standardized datasets for Flights, Passengers, and Tickets.
* **`dashboard/`**: The **`airline_ops_intelligence.pbix`** Power BI production file.
* **`documentation/`**: **`technical_deep_dive.pdf`** detailing the full system architecture.

---

**By integrating high-level data engineering with enterprise governance, this project serves as a blueprint for secure and scalable business intelligence.**
