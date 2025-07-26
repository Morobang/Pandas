# **Day 2: Series vs DataFrame - Simple Explanation**  

## **1. What is a Series?**  
📌 **A Series is like a single column in Excel.**  
- It holds **one type of data** (numbers, strings, etc.).  
- Has an **index** (row labels).  

### **How to Create a Series**  
```python
import pandas as pd

# From a list
ages = pd.Series([25, 30, 35, 40], name="Age")

# With custom index
grades = pd.Series([90, 85, 77], index=["Alice", "Bob", "Charlie"], name="Grades")
```

### **What Can You Do With a Series?**  
✔ Get values: `ages.values` → `[25, 30, 35, 40]`  
✔ Get index: `grades.index` → `["Alice", "Bob", "Charlie"]`  
✔ Filter: `ages[ages > 30]` → `35, 40`  

---

## **2. What is a DataFrame?**  
📌 **A DataFrame is like an entire Excel sheet.**  
- Made up of **multiple Series (columns)**.  
- Each column can have a different data type.  

### **How to Create a DataFrame**  
```python
# From a dictionary
data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 35],
    "City": ["NY", "LA", "Chicago"]
}
df = pd.DataFrame(data)

# With custom index
df = pd.DataFrame(data, index=["P1", "P2", "P3"])
```

### **What Can You Do With a DataFrame?**  
✔ View first rows: `df.head()`  
✔ Get a column: `df["Age"]` → Returns a **Series**  
✔ Filter rows: `df[df["Age"] > 25]`  

---

## **3. Key Differences**  
| Feature | **Series** | **DataFrame** |  
|---------|-----------|--------------|  
| **Shape** | 1D (single column) | 2D (multiple columns) |  
| **Index** | Yes (row labels) | Yes (row + column labels) |  
| **Use Case** | Single variable (e.g., "Age") | Entire dataset (e.g., "People Data") |  

### **Example:**
```python
# Series (just ages)
ages = pd.Series([25, 30, 35], name="Age")

# DataFrame (full table)
people = pd.DataFrame({
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 35]
})
```

---

## **4. Basic Inspection Methods**  
| Method | What It Does | Example |  
|--------|-------------|---------|  
| `.head(n)` | Shows first `n` rows | `df.head(2)` |  
| `.tail(n)` | Shows last `n` rows | `df.tail(1)` |  
| `.shape` | Returns (rows, columns) | `df.shape` → `(3, 2)` |  
| `.info()` | Data types & missing values | `df.info()` |  
| `.describe()` | Summary stats (mean, min, max) | `df.describe()` |  

### **Example Outputs:**
```python
print(df.shape)  # (3 rows, 3 columns)
print(df.info()) # Columns, data types, non-null counts
print(df.describe()) # Stats for numeric columns
```

---

## **5. When to Use Which?**  
- **Use a Series when:**  
  - Working with **a single column** (e.g., just "Age").  
  - Applying math operations (e.g., `grades.mean()`).  

- **Use a DataFrame when:**  
  - Handling **entire datasets** (e.g., Excel tables).  
  - Needing **multiple columns** (e.g., "Name", "Age", "City").  

---

## **6. Quick Quiz**  
1. **How do you create a Series from a list?**  
   → `pd.Series([1, 2, 3])`  

2. **How do you get the "Age" column from a DataFrame?**  
   → `df["Age"]`  

3. **What method shows the last 3 rows of a DataFrame?**  
   → `df.tail(3)`  

---

## **Summary**  
- **Series** = Single column of data.  
- **DataFrame** = Full table (multiple Series).  
- **Inspect data** with `.head()`, `.info()`, `.describe()`.  

**Next:** Learn how to filter and clean data in DataFrames! 🚀  

Would you like a **practice exercise** or **real-world example**? 😊