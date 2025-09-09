# 🤖 AI-Powered Corporate Spend Analysis for Fintech

### Project Overview

This project simulates a core product offering of a modern spend management fintech company (like Ramp, Brex, or Moniepoint). It involves a two-part analysis of a corporate credit card transaction dataset to uncover spending patterns and build an intelligent, automated expense categorization tool.

The goal is to demonstrate a full-stack data analysis workflow, from raw data processing to deriving actionable business insights and building a value-add AI feature.

-----

### The Business Problem

For any growing company, managing corporate spend is a critical challenge. Finance teams often face two major problems:

1.  **Lack of Spending Visibility:** Without clear analytics, it's difficult to identify areas of overspending, spot trends, or effectively manage budgets.
2.  **Manual Expense Categorization:** Employees and finance teams waste countless hours manually categorizing transactions, leading to errors and inefficiency.

This project tackles both problems by first performing a deep-dive analysis to provide visibility and then building a proof-of-concept AI tool to automate categorization.

-----

### Key Features

  * **Data Consolidation & Cleaning:** Ingested and merged 48 separate monthly CSV files into a master dataset, handling encoding errors and messy column structures.
  * **Exploratory Data Analysis (EDA):** Performed a comprehensive analysis to identify top spending categories and visualize monthly spending trends over time.
  * **Actionable Business Insights:** Derived three key strategic insights from the data that could help a finance team improve budget management and vendor negotiations.
  * **AI-Powered Categorization:** Developed a feature using **Google's Gemini API** to automatically standardize messy, official government expense categories into clean, modern business categories (e.g., "Travel, venue hire and exhibition services" → "Travel & Lodging").

-----

### Tech Stack

  * **Data Manipulation & Analysis:** Python, Pandas, NumPy
  * **Data Visualization:** Matplotlib, Seaborn
  * **AI & Machine Learning:** Google Gemini API (`google-generativeai`)
  * **Environment Management:** `dotenv` for API key management

-----

### Key Findings & Actionable Insights

#### Insight 1: Extreme Concentration in Travel Spend

A disproportionate amount of spending is concentrated in "Travel, venue hire and exhibition services." This single category's spending is more than the next four largest categories combined, highlighting a critical need for strong travel policies and better vendor negotiations.

`![Top Spending Categories](./images/top_categories_chart.png)`

#### Insight 2: Volatile and Seasonal Monthly Spending

The trend chart reveals significant volatility, with spending consistently peaking in January. This predictable seasonality makes manual budgeting difficult. A platform with real-time dashboards could help finance teams manage this volatility and prepare for seasonal cash flow demands.

`![Monthly Spending Trend](./images/monthly_spend_chart.png)`

#### Insight 3: Significant Spend in Core Operational Categories

Following travel, there is substantial spending in "Facilities" and "IT & Telecoms." These represent significant, recurring operational costs where even small optimizations could lead to major savings.

-----

### The AI-Powered Feature: Expense Categorization

A core feature of modern fintech platforms is the ability to intelligently categorize expenses. I built a proof-of-concept for this using a Large Language Model.

By providing the model with a few examples (a technique called few-shot prompting), it can accurately map inconsistent, legacy categories to a clean, standardized list. This automation saves time, reduces human error, and provides cleaner data for analysis.

**Example Mapping:**
| Original Government Category | AI-Generated Modern Category |
| :--- | :--- |
| `Travel, venue hire and exhibition services` | `Travel & Lodging` |
| `Human Resources` | `Recruitment & HR` |
| `IT & Telecoms` | `Software & Subscriptions` |
| `Facilities` | `Utilities` |

-----

### How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/YourUsername/YourRepoName.git
    cd YourRepoName
    ```
2.  **Set up the environment:**
      * It is recommended to use a virtual environment.
      * Install the required libraries:
        ```bash
        pip install -r requirements.txt
        ```
3.  **Set up your API Key:**
      * Create a `.env` file in the root directory.
      * Add your Google Gemini API key to the file:
        ```
        GEMINI_API_KEY="YOUR_API_KEY_HERE"
        ```
4.  **Run the Jupyter Notebook:**
      * Launch Jupyter Notebook and open the `AI-Powered Corporate Spend Analysis.ipynb` file.

-----
