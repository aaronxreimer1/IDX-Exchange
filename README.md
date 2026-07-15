# IDX-Exchange-DS-Project

## Project Objective

The goal of this project is to build and train a machine learning model to predict the **ClosePrice** (final sales price) of single residential properties in California using historical real estate data sourced from the California Regional Multiple Listing Service (CRMLS).

## Weekly Milestones & Progress

### Week 1: Orientation & Setup

* Analyzed the core assignment objectives and project scope.

* Retrieved a minimum of 6 months of historical CRMLSSold CSV data files.

* Examined the MetaData documentation to identify critical target features and column specifications.

### Week 2: Data Exploration

* Imported the 6-month real estate dataset into a Jupyter Notebook via pandas.

* Mapped out and analyzed distributions for the five core metrics: `ClosePrice`, `LivingArea`, `Bedrooms`, `Bathrooms`, and `LotSize`.

* Filtered the scope strictly to `PropertyType = "Residential"` and `PropertySubType = "Single Family Residence"` rows.

* **Deliverable:**

  * `01_exploration.ipynb` (Initial Jupyter Notebook detailing the exploratory data analysis plots).

### Week 3: Data Preprocessing

* Implemented clean data preprocessing routines by dropping listings completely missing critical values (ClosePrice, LivingArea) and applying median imputation to resolve missing categorical/numerical values (BedroomsTotal, BathroomsTotalInteger, LotSizeSquareFeet).

* Normalized numerical features (LivingArea, LotSizeSquareFeet, etc.) using StandardScaler to ensure a balanced, standardized feature set.

* Built a dynamic, rolling time-series train/test split, isolating the most recent month (May 2026) as the testing set and defining a tunable sliding historical window (X months) preceding it for model training.  

* **Deliverable:**

* 02_preprocessing.ipynb (Clean preprocessing pipeline and dynamic train/test splitting notebook).

* cleaned_sales_data.csv (Fully cleaned, normalized, and imputed master dataset exported for training).  

### Week 4: Baseline Model

* Evaluated predictions on the May 2026 test set using the Coefficient of Determination (R^2) metric to establish an initial performance benchmark.

* Documented training constraints, hyperparameter baselines (using a default 6-month historical window), and initial prediction variance metrics.  

* **Deliverable:**

* 03_baseline_model.ipynb (Jupyter Notebook demonstrating baseline model setup, evaluation run, and recorded R^2 performance).
