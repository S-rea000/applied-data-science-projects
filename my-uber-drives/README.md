# Data Processing & Analysis Projects

This repository contains multiple data analysis notebooks along with their corresponding CSV datasets. The work demonstrates simple data processing, API response handling logic, and exploratory data analysis using Python.

---

## 📊 Contents

### 1️⃣ Simple Data Processing
**Scenario:**  
Given login records:
```
userId, loginTime
101, 09:01
102, 09:05
101, 09:10
103, 09:15
101, 09:20
```

**Tasks Covered:**
- Count how many times each user logged in
- Return results in readable format
- Consider performance for large datasets

**Approach:**
- Use a dictionary (hash map) to count logins.
- Time Complexity: O(n)
- Scales efficiently for large data since lookup and updates are constant time.

**Example Output:**
```
User 101 logged in 3 times
User 102 logged in 1 time
User 103 logged in 1 time
```

---

### 2️⃣ API Response Handling

**Possible API Responses:**

Success:
```
{
  "status": "success",
  "data": { "name": "Asha" }
}
```

Error:
```
{
  "status": "error",
  "message": "User not found"
}
```

**Logic Handling:**

- If status = success:
  - Extract and display user data
- If status = error:
  - Print error message
  - Log error for debugging

**Sample Python Logic:**
```python
response = api_call()

if response["status"] == "success":
    print("User Name:", response["data"]["name"])
else:
    print("Error:", response["message"])
    with open("error_log.txt", "a") as log:
        log.write(response["message"] + "\n")
```

---

## 📁 Notebooks Included

- `customer-behaviour-analysis.ipynb`  
  Analysis of customer behavior dataset.

- `global-students-migration.ipynb`  
  Study of international student migration patterns.

- `my-uber-drives.ipynb`  
  Exploration and visualization of Uber trip data.

- `Untitled0.ipynb`  
  Basic processing and experimental work.

---

## 📂 Datasets

All CSV files used in analysis are stored in the `data/` folder.

---

## ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Jupyter Notebook

---

## 🚀 How to Run

1. Clone the repository:
```
git clone https://github.com/your-username/project-name.git
```

2. Open Jupyter Notebook:
```
jupyter notebook
```

3. Run any notebook inside the `notebooks/` folder.

---

## 📈 Scalability Notes

- Login counting uses a dictionary → handles millions of records efficiently.
- API error logging ensures traceability in production systems.
- CSV-based workflow supports batch data processing.
