# medallion-architecture-poc
 A data architecture project using the AdventureWorks dataset to implement Medallion Architecture, from raw data ingestion to business-ready insights with a focus on modelling, transformation, and governance.



---

##  Project Overview

###  Objective

To ingest, model, and transform the AdventureWorks dataset using a layered data architecture, demonstrating:

- Data pipeline architecture  
- Logical modeling  
- Entity-Relationship Diagram (ERD) design  
- Data quality and governance considerations

---

##  Project Structure


---

##  Dataset: AdventureWorks

The AdventureWorks dataset is a fictitious dataset by Microsoft that simulates a global manufacturing company selling bicycles and accessories. This project uses:

- 8 Excel worksheets split across two files  
- Includes tables like: Sales, Customers, Resellers, Products, Dates, Sales Territory, etc.

>  **Note**: Data source and Excel files are located in the `data/` directory.

---

##  Project Roadmap

### 1. Bronze Layer – Raw Data Ingestion

> *Objective: Ingest raw data into your chosen platform.*

- **Source**: Excel files from AdventureWorks  
- **Storage**: Microsoft Fabric Data Warehouse  
- **Ingestion Tool**: Microsoft Dataflow Gen2  
- **Automation**: Microsoft Fabric Data Factory  

**Considerations:**

- What data is being ingested?  
- Where is it stored?  
- How is it ingested?  
- How is it secured?

> **Tools Used**: Microsoft Fabric, OneDrive, Power BI, SQL Server (optional)

📸 **Screenshots Placeholder:**  
*Add screenshots of your ingestion flow in Fabric / Data Factory here*

---

### 2. Silver Layer – Data Modeling & Refinement

> *Objective: Organize, cleanse, and model data to prepare for analysis.*

- Consolidated 8 → 7 datasets by merging two customer files  
- Identified fact and dimension tables  
- Created a **Logical Data Model** representing relationships and keys  
- Built an **Entity Relationship Diagram (ERD)**

📁 **Files:**

- Logical Model: `models/logical_model.drawio`  
- ERD: `models/er_diagram.drawio` (or `.png` / `.pdf`)

📸 **Screenshots Placeholder:**  
*Add screenshots of your logical model and ERD here*

####  Relationship Summary

| Table           | Type       | Key Used               | Relationship     |
|----------------|------------|------------------------|------------------|
| Sales           | Fact       | SalesOrderLineKey      | Core fact table  |
| SalesOrder      | Dimension  | SalesOrderLineKey (PK) | 1:1 with Sales   |
| Customer        | Dimension  | CustomerKey            | 1:N with Sales   |
| Product         | Dimension  | ProductKey             | 1:N with Sales   |
| Reseller        | Dimension  | ResellerKey            | 1:N with Sales   |
| SalesTerritory  | Dimension  | SalesTerritoryKey      | 1:N with Sales   |
| Date            | Dimension  | DateKey                | 1:N with Sales   |

>  **Tip**: Look for primary and foreign keys; identify 1:1 or 1:N relationships.

📸 **Screenshots Placeholder:**  
*Add ERD visual here (from Draw.io, Lucidchart, etc.)*

---

### 3. Gold Layer – Curated Data for Insights

> *Objective: Deliver high-quality, business-ready data.*

- Transformed data for business usability  
- Final tables joined and cleaned

**Considerations:**

- Naming conventions  
- Data formatting  
- Aggregations and metrics (e.g. revenue, quantity sold)

 **Screenshots Placeholder:**  
*Add Power BI report, final dataset schema, or Fabric view here*

---

##  Data Governance & Security

Security and data governance are critical throughout all layers:

- **Data Storage**: Secure OneDrive folder with access control  
- **Workspace Access**: Managed via Microsoft Fabric permissions  
- **Monitoring & Lineage**: Tools like Microsoft Purview  
- **Duplication & Quality**: Merge & deduplicate customer tables  

**Scalability Considerations:**

- Can this scale in 5 years?  
- Are tools accessible by your team?

 **Screenshots Placeholder:**  
*Add screenshot of Purview dashboard, security settings, or Fabric workspace permissions here*

---

## 🛠 Tools Used

- **Microsoft Fabric** (Dataflow Gen2, Data Warehouse, Data Factory)  
- **Excel** (Source Files)  
- **Power BI** (Optional visualization)  
- **Draw.io / Lucidchart** (for ERD)  
- **Microsoft Purview** (Governance)

---

##  Success Criteria

To complete this project successfully, ensure the following:

-  Ingestion of raw data into the Bronze layer  
-  Development of a clear and accurate **Logical Model**  
-  Creation of a well-structured **Entity Relationship Diagram**  
-  Transformation and preparation of data in the Gold layer  
-  Implementation of data security and governance principles  
-  Demonstrated understanding of fact/dimension modeling

---

r


