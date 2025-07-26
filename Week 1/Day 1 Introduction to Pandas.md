# 🧼 **Day 1: Introduction to Pandas**

## 🧠 What is Pandas?

**Pandas** is a Python library built for **data analysis and manipulation**.

Think of it like Excel or SQL inside Python — but **faster, more flexible, and programmable**.

It gives you:

* Tables (`DataFrames`) like spreadsheets
* Tools to clean, reshape, summarize, and explore data
* Ways to read and write data from files like CSV, Excel, and databases

---

## 🎯 Why Use Pandas?

| Feature                        | Why It’s Useful                                               |
| ------------------------------ | ------------------------------------------------------------- |
| 🧾 **Handles Real-World Data** | You can clean messy datasets (nulls, typos, duplicates, etc.) |
| 🛠 **Easy Data Wrangling**     | Filter, group, aggregate, and join tables like SQL            |
| 📥 **Read/Write Many Formats** | Work with CSV, Excel, JSON, SQL, and more                     |
| 📊 **Basic Analysis Built-in** | Quickly get stats, trends, and visuals                        |
| 💨 **Fast + Pythonic**         | Works great with NumPy, Matplotlib, Seaborn, and scikit-learn |

---

## ⚙️ How to Install Pandas

If you're using **pip**:

```bash
pip install pandas
```

If you're using **Anaconda** (recommended for data science):

```bash
conda install pandas
```

If you're in **Jupyter Notebook**, try this:

```python
!pip install pandas
```

---

## 📦 Importing Pandas

Always import pandas like this:

```python
import pandas as pd
```

Why `pd`? It's the **standard nickname** used by the data community to keep code short.

You can now use pandas functions like `pd.DataFrame()`, `pd.read_csv()`, etc.

---

## 🔍 Basic Setup Example

Let’s create your first `Series` and `DataFrame`.

### 🔹 A Series = One Column

```python
import pandas as pd

sales = pd.Series([100, 200, 300, 400], name="Sales")
print(sales)
```

**Output:**

```
0    100
1    200
2    300
3    400
Name: Sales, dtype: int64
```

### 🔹 A DataFrame = Full Table

```python
data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Age": [25, 30, 35],
    "City": ["Cape Town", "Durban", "Joburg"]
}

df = pd.DataFrame(data)
print(df)
```

**Output:**

|   | Name    | Age | City      |
| - | ------- | --- | --------- |
| 0 | Alice   | 25  | Cape Town |
| 1 | Bob     | 30  | Durban    |
| 2 | Charlie | 35  | Joburg    |

---

## 🧠 Must-Know Functions (Setup Tools)

| Function        | What It Does                         |
| --------------- | ------------------------------------ |
| `df.head()`     | View first 5 rows of data            |
| `df.info()`     | Overview: columns, data types, nulls |
| `df.describe()` | Stats summary: mean, min, max, etc.  |
| `df.dtypes`     | Show data types                      |
| `df.columns`    | Show column names                    |

---

## ✅ Quick Recap

| Step | Task                                                         |
| ---- | ------------------------------------------------------------ |
| 1    | Install Pandas                                               |
| 2    | Import with `import pandas as pd`                            |
| 3    | Create a Series and a DataFrame                              |
| 4    | Use `.head()`, `.info()`, `.describe()` to explore your data |

---

Would you like:

* A **practice file** to try these out?
* A **quiz or checklist** to test yourself?
* The **Day 2 notes**?

Let me know how you’d like to keep going!
