Perfect! Here's your complete breakdown for:

---

# 📘 **Day 4: Data Inspection in Pandas**

---

## 🎯 Why Data Inspection?

Once your data is loaded (e.g. with `read_csv()`), you need to **inspect it** before cleaning or analysis.

This helps you:

* Understand the structure and size
* Spot missing or invalid values
* Detect column types and formats
* Check for outliers or unexpected values

---

## 🔍 Key Functions for Inspection

### 1️⃣ `.head()` → First 5 rows (by default)

```python
df.head()
```

✅ Use this to **peek at your data** and check column names & sample values.

You can also specify the number of rows:

```python
df.head(10)  # First 10 rows
```

---

### 2️⃣ `.tail()` → Last 5 rows (by default)

```python
df.tail()
```

✅ Useful to check **how data ends**, especially in time series or sorted datasets.

```python
df.tail(3)  # Last 3 rows
```

---

### 3️⃣ `.info()` → Structure, types, and memory usage

```python
df.info()
```

✅ Use this to understand:

* Number of rows
* Column names & types
* Count of non-null values
* Memory usage

🧪 Example Output:

```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 1000 entries, 0 to 999
Data columns (total 4 columns):
 #   Column     Non-Null Count  Dtype  
---  ------     --------------  -----  
 0   ID         1000 non-null   int64  
 1   Name       980 non-null    object 
 2   Age        970 non-null    float64
 3   Country    1000 non-null   object 
```

---

### 4️⃣ `.describe()` → Summary statistics (only for numeric columns by default)

```python
df.describe()
```

✅ Gives:

* Count, mean, std (standard deviation)
* min, max
* 25%, 50%, 75% percentiles

🧪 Example:

```
              Age       Salary
count  970.000000   970.000000
mean    29.352000  40000.000000
std      5.600000   8000.000000
min     18.000000  25000.000000
25%     26.000000  35000.000000
50%     30.000000  40000.000000
75%     33.000000  45000.000000
max     45.000000  60000.000000
```

🔁 To get `.describe()` for **non-numeric** columns (e.g., strings):

```python
df.describe(include='object')
```

Or for **all columns**:

```python
df.describe(include='all')
```

---

## 🛠 Bonus: Quick Checks

| Check                      | Code                          |
| -------------------------- | ----------------------------- |
| Shape of data              | `df.shape`                    |
| Column names               | `df.columns`                  |
| Data types                 | `df.dtypes`                   |
| Missing values             | `df.isnull().sum()`           |
| Value counts (categorical) | `df['column'].value_counts()` |

---

## ✅ Recap

| Function        | Purpose                              |
| --------------- | ------------------------------------ |
| `df.head()`     | See first few rows                   |
| `df.tail()`     | See last few rows                    |
| `df.info()`     | Structure and column overview        |
| `df.describe()` | Summary stats (mean, min, max, etc.) |

---

## 🧪 Practice Challenge

1. Load any dataset (`CSV`, `Excel`, or sample from seaborn)
2. Use `.head()` and `.tail()` to preview it
3. Run `.info()` to check data types and missing values
4. Use `.describe()` to check distributions

---

Would you like Day 5 next? (Working with `.columns`, `.index`, `.shape`, and `.dtypes`)
Or should I make a practice notebook for Day 4?
