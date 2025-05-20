# 🚀 Create and Use Dataflows (Gen2) in Microsoft Fabric

## Lab Purpose

The purpose of this lab was to understand and apply the fundamental features of **Dataflows (Gen2)** in Microsoft Fabric. Using a no-code approach via **Power Query Online**, I connected to an external CSV data source, applied data transformations, and loaded the data into a **Lakehouse**. I then used a **Data Pipeline** to orchestrate the flow. This lab provided a hands-on introduction to scalable data ingestion and transformation workflows in the cloud.

---

## ⚙️ Steps Followed

### 1. Create a Fabric Workspace
- Logged in to [Microsoft Fabric](https://app.fabric.microsoft.com/home?experience=fabric).
- Created a new workspace with trial capacity enabled.

### 2. Create a Lakehouse
- Created a new Lakehouse from the "Data Engineering" section.
- Gave it a unique and identifiable name.

### 3. Build a Dataflow (Gen2)
- Created a new **Dataflow Gen2** and opened it in Power Query Online.
- Imported data from a CSV file using the following URL:
  - `https://raw.githubusercontent.com/MicrosoftLearning/dp-data/main/orders.csv`
- Authentication: Anonymous
- Created a custom column named `MonthNo` using the formula:
  - `Date.Month([OrderDate])`
- Verified data types:  
  - `OrderDate`: Date  
  - `MonthNo`: Whole Number

### 4. Add a Data Destination
- Connected the dataflow to the previously created **Lakehouse**.
- Specified the destination table name as `orders`.
- Chose to append data with manual settings and published the dataflow.

### 5. Integrate with a Pipeline
- Created a **Data Pipeline** named `Load data`.
- Added a **Dataflow activity** and selected the previously created dataflow.
- Saved and ran the pipeline to ingest data into the lakehouse.

### 6. Verify Results
- Refreshed the tables in the lakehouse view.
- Verified the `orders` table was created and loaded with transformed data.

### 7. Clean Up Resources
- Deleted the workspace after completion to free up resources.

---

## 📚 What I Learned

- How to create and configure **Dataflows (Gen2)** in Microsoft Fabric.
- How to use **Power Query Online** for data transformation without writing code.
- How to connect to external data sources (e.g., CSV over HTTP).
- How to add calculated columns and manage data types in Power Query.
- How to link a dataflow to a **Lakehouse** as a data destination.
- How to use **Data Pipelines** to schedule and automate data ingestion steps.

---

## ✅ Key Technologies Used

- Microsoft Fabric (Trial)
- Lakehouse
- Dataflows Gen2 (Power Query Online)
- Data Pipelines
- CSV over HTTP

---

## Screenshot

<img width="1390" alt="2" src="https://github.com/user-attachments/assets/2d41654b-7282-4cc4-9139-278b1515dcf7" />

<img width="1421" alt="3" src="https://github.com/user-attachments/assets/f776e963-aa88-440a-b02a-99f50bad4c93" />

<img width="1422" alt="4" src="https://github.com/user-attachments/assets/49088dca-7d1d-4782-b027-25a50500222e" />

<img width="1462" alt="5" src="https://github.com/user-attachments/assets/1dc2df8a-a9ae-4770-8745-3b27ca6940e4" />

<img width="1424" alt="6" src="https://github.com/user-attachments/assets/661bdc91-587e-474c-af57-088a4fa0b9e0" />

<img width="1471" alt="7" src="https://github.com/user-attachments/assets/b5d9781f-6ff6-439b-80b8-91714e7fefe9" />

<img width="1464" alt="8" src="https://github.com/user-attachments/assets/28b19e4d-81d2-4b87-b917-23bdf3d678ea" />

<img width="1307" alt="9" src="https://github.com/user-attachments/assets/4b9c9914-e56c-4e96-9291-2177f165cdb5" />

<img width="1192" alt="10" src="https://github.com/user-attachments/assets/177ad6eb-b9ce-4f1e-bf2c-d8ad8f4cf26d" />

<img width="1457" alt="11" src="https://github.com/user-attachments/assets/29823d8d-7ad0-4a85-b2bd-25ec2e1c02a4" />

<img width="1472" alt="12" src="https://github.com/user-attachments/assets/49c5b617-8f5e-4d1b-8e64-6dc6e368369a" />

<img width="1475" alt="13" src="https://github.com/user-attachments/assets/8fed116e-3aed-4a5a-8204-77211f41715c" />

<img width="1452" alt="14" src="https://github.com/user-attachments/assets/e9a59e7b-86f9-4ac0-b5eb-468b68fd003e" />

<img width="898" alt="15" src="https://github.com/user-attachments/assets/4d022890-d944-49a6-a3e1-7d62431f43fa" />


