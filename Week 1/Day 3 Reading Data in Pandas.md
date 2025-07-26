# **Day 3: Reading Data in Pandas**

## Why Reading Data is Important

Before you clean or analyze anything, you need to **load your data into Python**.

Pandas makes it **very easy to read data** from:

* CSV files
* Excel files
* SQL databases
* JSON, HTML, clipboard, and more

---

## Most Common: Reading a CSV File

### Syntax:

```python
import pandas as pd

df = pd.read_csv("filename.csv")
```

### Example:

```python
df = pd.read_csv("sales_data.csv")
print(df.head())
```

This reads the file `sales_data.csv` into a **DataFrame** called `df`.

---

## File Path Tips

| Type        | Example                             |
| ----------- | ----------------------------------- |
| Same folder | `"mydata.csv"`                      |
| Subfolder   | `"data/mydata.csv"`                 |
| Full path   | `"C:/Users/You/Desktop/mydata.csv"` |
| Online file | `"https://example.com/file.csv"`    |

You can also upload the file into Colab or Jupyter using:

```python
from google.colab import files
uploaded = files.upload()
```

---

## Common `read_csv()` Options

| Option                         | Use                                                  |
| ------------------------------ | ---------------------------------------------------- |
| `sep=";"`                      | Use a different separator (e.g., `;` instead of `,`) |
| `header=None`                  | If the file has **no column headers**                |
| `names=["A", "B", "C"]`        | Set your own column names                            |
| `index_col=0`                  | Use the first column as the row index                |
| `usecols=["A", "B"]`           | Load only selected columns                           |
| `nrows=10`                     | Read only the first 10 rows                          |
| `na_values=["-", "NA", "n/a"]` | Define what should count as NaN                      |

### Example:

```python
df = pd.read_csv("sales.csv", na_values=["NA", "-"])
```

---

## Reading Excel Files

```python
df = pd.read_excel("data.xlsx")
```

> Requires `openpyxl` or `xlrd` installed:

```bash
pip install openpyxl
```

---

## Read Data from a Dictionary or List (without file)

```python
data = {
    "Name": ["Alice", "Bob", "Charlie"],
    "Score": [85, 92, 78]
}

df = pd.DataFrame(data)
print(df)
```

---

## Quick Checks After Reading

| Check          | Code                |
| -------------- | ------------------- |
| First 5 rows   | `df.head()`         |
| Shape          | `df.shape`          |
| Column names   | `df.columns`        |
| Data types     | `df.dtypes`         |
| Missing values | `df.isnull().sum()` |

---

## Recap

| Task           | Code                                 |
| -------------- | ------------------------------------ |
| Read CSV       | `pd.read_csv("file.csv")`            |
| Read Excel     | `pd.read_excel("file.xlsx")`         |
| Inspect Data   | `df.head()`, `df.info()`, `df.shape` |
| Handle missing | `na_values`, `.isnull()`             |

---

## Practice Challenge

1. Download or create a CSV file (e.g., `students.csv`)
2. Load it into pandas
3. Show:

   * First 5 rows
   * Number of rows/columns
   * Columns with missing values

