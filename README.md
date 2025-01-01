
# Association Rules in Machine Learning

## Overview
This repository demonstrates the application of Association Rule Mining algorithms on an online retail dataset. The project includes:

1. **Loading and preprocessing the dataset**: A dataset containing transactions from a UK-based online retailer.
2. **Exploratory Data Analysis (EDA)**: Analyzing the dataset to uncover trends, patterns, and insights.
3. **Implementation of Machine Learning algorithms**: Applying three popular association rule mining algorithms (Apriori, FP-Growth, and Eclat) to identify relationships between items in transactions.

---

## Dataset
### **Source:**
The dataset, `Online Retail II`, contains transactional data of a UK-based non-store online retailer from **01/12/2009 to 09/12/2011**. 

### **Attributes:**
- **InvoiceNo**: Unique invoice number; invoices starting with 'C' indicate cancellations.
- **StockCode**: Unique product code.
- **Description**: Name of the product.
- **Quantity**: Number of items per transaction.
- **InvoiceDate**: Date and time of the transaction.
- **UnitPrice**: Price per unit in GBP (£).
- **CustomerID**: Unique identifier for customers.
- **Country**: Customer’s country of residence.

---

## Project Workflow

### **1. Data Loading and Cleaning**
- Handled missing values, including rows with missing `CustomerID`.
- Removed duplicate entries and transactions marked as cancellations.
- Ensured all quantities and unit prices were positive.

### **2. Exploratory Data Analysis (EDA)**
- Visualized transaction frequency, most purchased items, and revenue distribution.
- Generated heatmaps and bar charts to understand customer purchasing behavior.
- Analyzed trends by time and country.

### **3. Algorithms Used**
#### **1. Apriori Algorithm**
- Identified frequent itemsets using a bottom-up approach.
- Generated association rules by applying support and confidence thresholds.
- Efficient for smaller datasets.

#### **2. FP-Growth Algorithm**
- Built a compact Frequent Pattern Tree (FP-Tree) for dataset compression.
- Extracted frequent itemsets directly from the FP-Tree without candidate generation.
- Scalable and efficient for large datasets.

#### **3. Eclat Algorithm**
- Calculated support using intersections of transaction IDs.
- Worked in a depth-first search manner.
- Memory-efficient for dense datasets.

---

## Results and Insights
- **Frequent Itemsets**: Items frequently purchased together (e.g., gift sets, decorative items).
- **Association Rules**: Discovered meaningful rules such as "If a customer buys `Item A`, they are likely to buy `Item B`".
- **Performance Comparison**: FP-Growth was the fastest, while Apriori provided more customizable results.

---

## Files in the Repository
- `dataset.csv`: The raw dataset used for the analysis.
- `notebook.ipynb`: Contains the code for loading, cleaning, EDA, and applying algorithms.
- `results/`: Folder containing output files (e.g., frequent itemsets and rules).
- `Association_Rules_Presentation.pptx`: A presentation summarizing the project.
- `README.md`: Overview of the project.

---

## How to Use

1. **Clone the repository**:
   ```bash
   git clone https://github.com/thisismohsinsyed/association-rule-algorithms-with-python-implementation.git
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the notebook**:
   Open `notebook.ipynb` in Jupyter Notebook and execute the cells.

4. **Explore the results**:
   - Generated association rules are saved in the `results/` folder.
   - Visualizations are displayed within the notebook.

---

## Requirements
- Python 3.7+
- Jupyter Notebook
- Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, mlxtend

---

## Future Improvements
- Add visualization of rules using network graphs.
- Experiment with varying thresholds for support and confidence.
- Apply additional datasets to test the robustness of the algorithms.

---

## Acknowledgments
- Dataset provided by the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets.php).

---

## License
This project is licensed under the MIT License - see the `LICENSE` file for details.
