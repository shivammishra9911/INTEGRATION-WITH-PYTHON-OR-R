# INTEGRATION-WITH-PYTHON-OR-R

 COMPANY: CODTECH IT SOLUTIONS PVT.LTD

 NAME: Shivam Mishra

 INTERNID: CT12PFA

 DOMAIN: POWER BI

 DURATION: 8 WEEKS

 MENTOR: NEELA SANTOSH

![Image](https://github.com/user-attachments/assets/b0730a6f-4129-4557-ad5c-50dd23cd33a5)
![Image](https://github.com/user-attachments/assets/ac252533-b34e-4a07-859e-9c0c128e8771)
![Image](https://github.com/user-attachments/assets/ec32fd36-f2cb-4206-95e7-50809b5ba070)
![Image](https://github.com/user-attachments/assets/43c3463a-0712-4f4c-9e4b-9dae2a2810b8)

## **Disaster Data Analysis Project Using Python and Power BI**

This project integrates **Python scripting** with **Power BI** to create a **data-driven disaster analysis dashboard**. It leverages **synthetically generated disaster data** to visualize trends, severity, estimated damages, and geographical distribution of various disasters. Below is a detailed breakdown of how the project was developed, the technologies used, and its significance.

---

### **1. Python Script for Data Generation**
Since real-world disaster data may not always be available in an easily accessible format, this project **uses Python to generate synthetic disaster data**. The script creates **500 records** containing details about different disaster events.

#### **1.1. Importing Required Libraries**
```python
import pandas as pd
import numpy as np
from datetime import datetime, timedelta
```
- **Pandas**: Used for handling and storing the dataset.
- **NumPy**: Used for generating random selections.
- **Datetime**: Helps generate random dates for disasters.

---

#### **1.2. Generating Random Disaster Data**
- **Random Dates**: A list of random dates in **2023** is created.
- **Disaster Types**: Events like Earthquake, Flood, Wildfire, Hurricane, and Tornado are randomly assigned.
- **Severity Levels**: Each disaster is categorized into **Low, Moderate, High, or Severe**.
- **Location**: A random state in the **USA** is assigned.
- **Estimated Damage**: A random value (in millions) estimates financial losses.

```python
start_date = datetime(2023, 1, 1)
date_list = [start_date + timedelta(days=np.random.randint(0, 365)) for _ in range(500)]

disaster_types = ['Earthquake', 'Flood', 'Wildfire', 'Hurricane', 'Tornado']
disaster_list = np.random.choice(disaster_types, 500)

severity_levels = ['Low', 'Moderate', 'High', 'Severe']
severity_list = np.random.choice(severity_levels, 500)

locations = ['New York', 'California', 'Texas', 'Florida', 'Illinois', 'Ohio', 'Michigan', 'Nevada', 'Washington']
location_list = np.random.choice(locations, 500)

damage_values = np.random.randint(1, 100, 500)  # Damage in millions
```
---

#### **1.3. Creating a DataFrame & Exporting CSV**
The generated data is stored in a **Pandas DataFrame** and then **exported as a CSV file** to be used in Power BI.

```python
df = pd.DataFrame({
    'Date': date_list,
    'Disaster_Type': disaster_list,
    'Severity': severity_list,
    'Location': location_list,
    'Estimated_Damage_Million': damage_values
})

df.to_csv('disaster_data.csv', index=False)
print("Dataset 'disaster_data.csv' created successfully.")
```
**Output File**: `disaster_data.csv` (Contains 500 rows of disaster event data).

---

### **2. Integrating Python Data into Power BI**
Once the dataset is generated, it is **imported into Power BI** for visualization.

#### **2.1. Importing the Dataset**
In Power BI:
1. Click **"Get Data" → "Text/CSV"**.
2. Select `disaster_data.csv`.
3. Load the data into Power BI.

#### **2.2. Data Model Structure**
The dataset contains the following **columns**:
- **Date**: Timestamp of the disaster event.
- **Disaster_Type**: Type of disaster.
- **Severity**: Categorized as **Low, Moderate, High, Severe**.
- **Location**: US state where the disaster occurred.
- **Estimated_Damage_Million**: Financial impact in millions.

---

### **3. Creating a Power BI Dashboard**
Once the data is imported, multiple **visualizations** are created to analyze disaster trends and impact.

#### **3.1. Key Metrics & KPIs**
The following **key performance indicators (KPIs)** are calculated:
- **Total Number of Disasters**: 500 (Total Count)
- **Sum of Estimated Damage**: **25.07K Million** (Total damage cost)
- **Disaster Trend Over Time**: A time-series trend of disasters occurring throughout **2023**.

---

#### **3.2. Visualizations**
1. **Disaster Count by Type** (Bar Chart)
   - Displays how many times each disaster type occurred.
   - Example: **Earthquakes (110 occurrences), Wildfires (109 occurrences)**.

2. **Disaster Trend Over Time** (Line Chart)
   - Shows disaster occurrences **month-wise** across the year.

3. **Disasters by Location** (Map Visualization)
   - Displays disasters on a **map of the USA**.
   - Different disasters are color-coded.

4. **Cities With Most Disasters** (Bar Chart)
   - Shows which US states had the most disaster events.
   - Example: **Ohio (62), Nevada (58), Texas (50), New York (49), Washington (49)**.

5. **Estimated Damage by Disaster Type** (Column Chart)
   - Compares total financial losses per disaster type.

6. **Severity Distribution** (Pie Chart)
   - Shows the percentage distribution of disaster severities.
   - Example: **Each severity level has nearly 25% share**.

---

### **4. Significance & Insights**
This project showcases how **Python can be used for data simulation and Power BI for visualization**, providing the following benefits:
1. **Data-Driven Decision Making**: Governments and organizations can identify high-risk disaster zones and allocate resources accordingly.
2. **Real-time Analysis**: The same approach can be used with **live data sources (APIs)** to track disasters in real time.
3. **Automated Reporting**: The dashboard can be scheduled for automatic updates, helping emergency response teams take timely action.
4. **Financial Impact Estimation**: The **damage cost analysis** can help with **insurance, relief funds, and policy planning**.

---

### **5. Possible Enhancements**
- **Machine Learning Predictions**: Use **historical disaster data** to predict future disasters.
- **Integration with Weather & Climate APIs**: Fetch **real-time disaster alerts**.
- **Advanced Mapping Techniques**: Use **Geospatial analysis** to pinpoint disaster-prone areas.
- **Dynamic Filtering**: Allow users to select specific disaster types or time periods for customized insights.

---

### **6. Conclusion**
This project successfully integrates **Python-generated data** with **Power BI dashboards**, showcasing how **synthetic disaster data** can be visualized for meaningful insights. It demonstrates the **power of Python scripting for data generation** and **Power BI’s interactive reporting capabilities**, making it a **valuable tool for disaster management and risk assessment**.

Would you like additional enhancements, such as **forecasting future disasters or adding real-time data sources**? 🚀
