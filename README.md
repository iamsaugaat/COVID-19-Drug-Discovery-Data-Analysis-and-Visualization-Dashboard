# COVID-19 Drug Discovery – Data Analysis and Visualization Dashboard

## Overview
This project analyzes molecular data from a publicly available COVID-19 drug discovery dataset.  
Using data science workflows (Python, pandas, scikit-learn) and visual analytics (Seaborn, Matplotlib, Streamlit), explored the physicochemical properties of drug-like compounds and their relationship with antiviral activity (`pIC50`).  

The results include **statistical insights, visual exploration, and a fully interactive dashboard** for filtering compounds and exploring correlations between molecular properties and activity.  

This workflow mirrors **real-world biotherapeutic research**, where early-stage compound data is assessed for trends and potential lead optimization.

---

## Key Achievements

### 1. **Data Curation and Quality Checks**
- Standardized **104 compounds** with **40 properties** each (molecular descriptors from PubChem).
- Cleaned `pIC50` activity values by removing non-numeric or blinded entries.
- Handled missing values to ensure accurate analysis.

---

### 2. **Exploratory Data Analysis (EDA)**

**a) Molecular Weight Distribution**  
<img width="773" height="490" alt="Molecular Weight Distribution" src="https://github.com/user-attachments/assets/76d4a780-4fd8-41bc-bfd4-f3b0d6091360" />

- Visualizes the range of molecular weights.  
- Most compounds fall between **300–450 Da**, aligning with drug-likeness criteria (Lipinski’s rule).  

**b) Pairwise Relationships**  

- Scatter matrix showing **trends between molecular descriptors** (Molecular Weight, LogP, Exact Mass).  
- Clear linear relationships between **Exact Mass** and **Monoisotopic Mass**, as expected.  

---

### 3. **Correlation Insights**

**Correlation Heatmap**  
<img width="547" height="506" alt="correlation_heatmap" src="https://github.com/user-attachments/assets/40aa42f6-2dd9-4520-ae8e-9e292277b218" />

- Comprehensive matrix of correlations between **molecular properties** and **pIC50**.  
- **Key Insight:**  
  - Features like `XStericQuadrupole3D`, `FeatureAnionCount3D`, and `ConformerCount3D` show weak-to-moderate positive correlations with `pIC50`.  
  - This suggests potential structural/3D properties influencing activity.

---

### 4. **Predictive Modeling**

**Feature Importance Analysis**  
- Built a **baseline Random Forest Regressor** to estimate activity (`pIC50`).  
- While the dataset size limited predictive accuracy (R² ≈ -0.1), the **model highlights which features may be worth exploring further**, e.g., **stereochemistry-related 3D descriptors**.

---

### 5. ** Dashboard (Streamlit)**  
<img width="565" height="698" alt="Dashboard" src="https://github.com/user-attachments/assets/ed803486-50f7-4334-b991-1d670bbdb512" />

- A live app allowing:
  - Filtering compounds by **molecular weight**.
  - Inspecting **distribution plots** dynamically.
  - Viewing **correlation heatmaps** for filtered subsets.  

This interactive view is ideal for **scientists and decision-makers** to quickly focus on compounds with desirable properties.

---

## Deliverables

- **Notebook**: `analysis.ipynb` – Full data cleaning, exploration, and modeling.
- **Datasets**: `DDH Data` and `DDH Data with Properties`
- **Figures**:  
  - `molecular_weight_distribution.png`
  - `pairplot.png`
  - `correlation_heatmap.png`
  -   - `Dashboard.png`

---

## Value
This project demonstrates:
- **Data-driven decision support** in drug discovery.
- How **data science tools can highlight trends** in molecular datasets.
- **A reusable framework** for exploring early-stage chemical/biotherapeutic data.

Such analyses are fundamental to **prioritizing promising compounds, understanding structural-property relationships, and accelerating R&D pipelines**.
