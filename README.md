# FIFA 21 Data Wrangling and Preprocessing Pipeline

## Project Overview
This repository demonstrates applied data management, cleaning, and preprocessing techniques using Python and Pandas. The project takes a highly unorganized, messy dataset containing information on over 18,000 FIFA 21 players and transforms it into a clean, structured, and analysis-ready format. 

This project was built to showcase core data engineering competencies, including schema standardization, string manipulation, data type casting, and the development of custom parsing algorithms for mixed-format data.

## Dataset
The data used in this project is the **FIFA 21 Messy Dataset** sourced from Kaggle. It contains 77 features (columns) for 18,979 players, originally riddled with inconsistent data types, hidden text artifacts, mixed measurement units, and redundant characters.

## Key Data Management Techniques Applied
* **Schema Standardization:** Reformatted all 77 column headers to a standardized snake_case format (e.g., stripping whitespaces, replacing spaces with underscores) and mapped ambiguous headers to descriptive names (e.g., `↓ova` to `overall`, `a/w` to `attacking_work_rate`).
* **Custom Data Parsing:** Developed a custom Python function to parse the `Height` column, which contained mixed formats (both feet/inches strings and centimeter strings), standardizing all values into numeric centimeter floats.
* **Feature Extraction:** Engineered structured variables from raw text data. For example, parsed the comma-separated `Positions` string to isolate a `primary_position`, and split the `Contract` string to create distinct `contract_start`, `contract_end`, and `contract_status` columns.
* **Data Type Conversion:** Systematically cleaned and casted object types to integers, floats, and datetime objects. This included stripping currency symbols (`€`) and magnitude letters (`M`, `K`) from financial columns (`Value`, `Wage`, `Release Clause`) to enable numerical aggregation.
* **Text & Categorical Standardization:** Cleaned hidden text artifacts (like `\n` characters in the `Club` column) and stripped special characters (like `★` in skill rating columns) to ensure data integrity.

## Technologies Used
* **Python 3.x**
* **Pandas** (Data manipulation, cleaning, and structural operations)
* **NumPy** (Handling missing values and numerical transformations)
* **Jupyter Notebook** (Interactive development and documentation)

## How to Run the Project
1. Clone this repository to your local machine.
2. Ensure you have Python and the required libraries installed (`pip install pandas numpy`).
3. Download the raw data file (`fifa21_raw_data_v2.csv`) and place it in the designated `Data/` directory.
4. Open `FIFA21_Data_Cleaning.ipynb` in Jupyter Notebook or JupyterLab and execute the cells sequentially.

## Author
**Ea Bunleang**
*Undergraduate, Data Science and Engineering*
