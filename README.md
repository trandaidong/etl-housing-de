# 🏠 Housing Price ETL Project

This project is a small-scale **Data Engineering pipeline** built to perform **ETL (Extract, Transform, Load)** on a dataset of house sales. The dataset is sourced from Kaggle and includes information on house prices and features such as the number of bedrooms, square footage, and more.

## 📌 Project Objectives

- Download housing data automatically using `kagglehub`.
- Perform basic cleaning and preprocessing.
- Conduct exploratory analysis on key attributes.
- Present average housing prices grouped by bedroom count.
- Serve as a foundational project for learning ETL concepts.

---

## 📂 Dataset

- **Source**: [Kaggle - House Sales in King County, USA](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction)
- **Fields**: Includes features like `price`, `bedrooms`, `bathrooms`, `sqft_living`, `zipcode`, etc.
- **Size**: ~21 features, ~21,000 records

---

## 🛠️ Technologies Used

| Tool          | Purpose                         |
|---------------|----------------------------------|
| Python        | Core programming language       |
| Pandas        | Data manipulation & cleaning    |
| KaggleHub     | Dataset fetching                |
| tqdm          | Progress bars                   |
| Jupyter       | Notebook-based development      |

---

## 🔁 ETL Workflow

### 1. **Extract**

- Dataset downloaded using `kagglehub`:
  ```python
  path = kagglehub.dataset_download("harlfoxem/housesalesprediction")
### 2. Transform
- Convert date strings to datetime
- Drop missing values
- Filter records with invalid price
- Explore unique values (e.g., bedrooms)
- Group by bedrooms and calculate avg(price)
### 3. Loads
