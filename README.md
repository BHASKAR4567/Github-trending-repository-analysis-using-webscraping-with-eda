# GitHub Trending Repositories — Web Scraping & EDA

A Python-based Web Scraping and Exploratory Data Analysis project that collects GitHub repository data across different technology categories and topics using **Requests and BeautifulSoup**. The scraped data is cleaned and analyzed using **Pandas and NumPy** to understand repository popularity based on GitHub Stars.

## 📌 Project Overview

GitHub contains thousands of repositories across different technologies, topics, and programming languages. This project automates the collection of repository information from GitHub topic pages and performs data analysis to identify popularity patterns across technology categories, topics, and programming languages.

The project collected **781 GitHub repositories with 7 columns**:

* Category
* Topic
* Repository
* Owner
* Repository URL
* Language
* Stars

## 🎯 Objectives

* Collect GitHub repository data through web scraping.
* Analyze repository popularity using GitHub Stars.
* Compare repository popularity across technology categories and topics.
* Identify the most represented programming languages.
* Clean and preprocess the scraped dataset.
* Analyze relationships between repository features and Stars.
* Perform statistical and hypothesis testing.
* Generate meaningful business insights from the analysis.

## 🛠️ Technologies Used

* **Python**
* **Requests**
* **BeautifulSoup**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **SciPy**

## 🌐 Web Scraping

GitHub topic pages were accessed using the **Requests** library and parsed using **BeautifulSoup**.

The scraper extracts:

* Repository name
* Repository owner
* Repository URL
* Programming language
* GitHub Stars
* Category
* Topic

A `seen_urls` set was used to avoid collecting the same repository multiple times. The scraper also handles GitHub Star values such as `k` and `m` formats and converts them into numerical values.

## 🧹 Data Preprocessing

The scraped dataset was checked and prepared before performing EDA.

The preprocessing steps include:

* Checking missing values
* Handling missing programming-language values
* Checking duplicate records
* Converting Stars into numeric format
* Checking invalid values such as negative Stars
* Cleaning categorical values
* Detecting potential outliers using the IQR method

## 📊 Exploratory Data Analysis

### Univariate Analysis

Analyzed individual variables such as:

* Distribution of GitHub Stars
* Top programming languages
* Repository popularity

The analysis showed that most repositories have relatively fewer Stars, while a small number of repositories have exceptionally high Star counts.

### Bivariate Analysis

Analyzed relationships such as:

* Average Stars by Category
* Category-wise repository popularity
* Repository features vs Stars

**Web Development** showed the highest average repository popularity in the analyzed dataset, followed by **Data Science**.

### Multivariate Analysis

Multiple repository features were analyzed together to understand popularity patterns across categories, languages, and repository characteristics.

## 🔎 Feature Engineering

Additional features were created to support deeper analysis, including:

* `Log_Stars`
* Repository Name Length
* Owner Name Length
* Repository Word Count

`Log_Stars` was created to provide a compressed representation of the highly skewed Star distribution.

## 📈 Correlation Analysis

Correlation analysis was performed to understand relationships between numerical features.

Key findings:

* Repository Name Length and Repo Word Count showed a strong positive correlation.
* Repository Name Length had almost no relationship with Stars.
* Owner Name Length had almost no relationship with Stars.
* Stars and Log_Stars showed a positive correlation because Log_Stars was derived from Stars.

## 🧪 Statistical & Hypothesis Testing

The project also includes statistical analysis using:

### Independent T-Test

Compared GitHub Stars between **Python and Java repositories**.

### Chi-Square Test

Examined whether **Category and Language** are statistically associated.

### ANOVA

Compared average GitHub Stars across different **technology categories**.

The statistical tests produced significant results at the 0.05 significance level for the tested relationships.

## 💡 Key Insights

* **Web Development** has the highest average repository popularity in the dataset.
* **Python, TypeScript, and JavaScript** are among the most represented programming languages.
* GitHub Stars are highly varied and right-skewed.
* A small number of repositories account for exceptionally high Star counts.
* Repository naming characteristics have little relationship with repository popularity.
* Category and programming language show a statistically significant association.
* Average repository Stars differ significantly across technology categories.

## 📁 Project Structure

```text
GitHub-Web-Scraping-EDA/
│
├── EDA GITHUBmain.ipynb
├── github_topics_scraped.csv
├── GitHub_Web_Scraping_EDA_Presentation.pptx
└── README.md
```

### Files Description

| File                                        | Description                                                                                                                                     |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| `EDA GITHUBmain.ipynb`                      | Jupyter Notebook containing the complete web scraping, data cleaning, EDA, feature engineering, correlation analysis, and statistical analysis. |
| `github_topics_scraped.csv`                 | Scraped GitHub repository dataset containing 781 repositories and 7 columns.                                                                    |
| `GitHub_Web_Scraping_EDA_Presentation.pptx` | Project presentation explaining the objective, methodology, data preprocessing, EDA, statistical analysis, insights, and conclusion.            |
| `README.md`                                 | Project documentation containing an overview, technologies, workflow, analysis, insights, and project structure.                                |

## 🚀 Project Workflow

```text
GitHub Topic Pages
       ↓
Requests
       ↓
BeautifulSoup
       ↓
Data Collection
       ↓
Data Cleaning & Preprocessing
       ↓
Exploratory Data Analysis
       ↓
Visualization
       ↓
Feature Engineering
       ↓
Correlation Analysis
       ↓
Statistical Testing
       ↓
Business Insights
```

## 📌 Conclusion

This project demonstrates how web scraping and data analytics can be combined to collect and analyze real-world GitHub repository data. The analysis provides insights into repository popularity, programming-language distribution, technology categories, and statistical relationships within the scraped dataset.
