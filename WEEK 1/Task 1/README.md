# AI & ML Internship – Task 1: Data Cleaning and Preprocessing

## Project Overview

This project focuses on data cleaning, exploration, and preprocessing using the **Titanic dataset**. It demonstrates essential data preparation techniques using Python and popular data science libraries.

The main objective is to transform raw data into a clean and structured format suitable for machine learning.

This project covers missing-value handling, categorical encoding, feature scaling, outlier detection, and final data validation.

## Objectives

- Understand and explore a real-world dataset.
- Identify and handle missing values.
- Detect and investigate duplicate records.
- Convert categorical variables into numerical representations.
- Apply feature scaling techniques.
- Detect and investigate potential outliers.
- Prepare numerical and categorical features for machine learning.
- Build a preprocessing workflow while avoiding data leakage.

## Technologies and Tools

The project uses the following technologies:

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical computations |
| Matplotlib | Data visualization |
| Seaborn | Statistical data visualization |
| Scikit-learn | Data preprocessing and machine learning utilities |
| SciPy | Statistical computations |
| Jupyter Notebook | Interactive development environment |
| Git & GitHub | Version control and project hosting |

## Dataset Description

The project uses the Titanic passenger dataset.

The dataset contains passenger information, including:

- PassengerId
- Survived
- Pclass
- Name
- Sex
- Age
- SibSp
- Parch
- Ticket
- Fare
- Cabin
- Embarked

The target variable is **Survived**:

- `0`: Passenger did not survive.
- `1`: Passenger survived.

The dataset is stored in the `dataset/` directory.

## Project Structure

```text
AI-ML-Internship-Task-1/
│
├── dataset/
│   └── titanic.csv
│
├── notebooks/
│   └── data_cleaning.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

## Tasks Performed

### 1. Data Loading and Exploration

- Imported the required Python libraries.
- Loaded the Titanic dataset using Pandas.
- Examined the first and last records.
- Checked dataset dimensions and column names.
- Inspected data types and statistical summaries.
- Identified missing values and duplicate records.

### 2. Missing Value Handling

- Identified missing values in the dataset.
- Examined the distribution of missing data.
- Used median imputation for the `Age` column.
- Used mode imputation for the `Embarked` column.
- Removed the `Cabin` column because of its high proportion of missing values.

### 3. Categorical Data Encoding

Explored techniques for converting categorical variables into numerical representations.

Techniques included:

- Label encoding.
- One-Hot Encoding.

Categorical features such as `Sex`, `Embarked`, and `Pclass` were prepared for numerical machine learning workflows.

### 4. Feature Scaling

Explored two feature scaling techniques:

- **Standardization:** Using `StandardScaler` to transform numerical features based on their mean and standard deviation.
- **Normalization:** Using `MinMaxScaler` to scale values into a specified range.

The selected numerical features included `Age`, `Fare`, `SibSp`, and `Parch`.

### 5. Outlier Detection and Treatment

Investigated potential outliers using:

- Boxplots.
- Histograms.
- Interquartile Range (IQR).
- Z-score.

Explored different outlier treatment techniques:

- Outlier removal.
- Outlier capping.
- Logarithmic transformation.

The `Fare` feature was also examined using logarithmic transformation to reduce right skewness.

Potentially valid passenger observations were retained rather than automatically removing all records flagged as outliers.

### 6. Final Data Preprocessing and Validation

Prepared the dataset for a machine learning workflow by:

- Separating input features (`X`) and target variable (`y`).
- Splitting the data into training and testing sets.
- Using an 80/20 train-test split.
- Applying median imputation and standardization to numerical features.
- Applying most-frequent imputation and One-Hot Encoding to categorical features.
- Combining preprocessing operations using `ColumnTransformer`.
- Building preprocessing workflows using Scikit-learn `Pipeline`.
- Checking transformed feature dimensions and data quality.

The preprocessing workflow was fitted on the training data and applied to the testing data to help prevent data leakage.

## Installation and Setup

### Prerequisites

- Python 3.9 or later.
- Visual Studio Code or Jupyter Notebook.
- Git.

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/AI-ML-Internship-Task-1.git
```

### 2. Navigate to the project directory

```bash
cd AI-ML-Internship-Task-1
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the virtual environment

**Windows:**

```bash
venv\Scripts\activate
```

**Linux/macOS:**

```bash
source venv/bin/activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/data_cleaning.ipynb
```

Run the notebook cells sequentially to reproduce the analysis.

## Key Learning Outcomes

Through this project, I gained practical experience in:

- Data exploration and quality assessment.
- Handling missing and duplicate data.
- Categorical variable encoding.
- Numerical feature scaling.
- Statistical outlier detection.
- Feature transformation.
- Scikit-learn preprocessing pipelines.
- Training and testing data separation.
- Preventing data leakage during preprocessing.

## Project Status

**Completed:** Data cleaning and preprocessing workflow.

This project focuses on data preparation. Training and evaluating a predictive machine learning model are outside the scope of this task.

## Author

**Jules Kitenge Kiayima**

Computer Science Undergraduate | Data Science | Machine Learning | Artificial Intelligence

- GitHub: https://github.com/juleskkayima
- LinkedIn: https://linkedin.com/in/juleskitengek/

---

*This project was completed as part of an AI & ML internship task to develop practical skills in data cleaning and preprocessing using Python.*
