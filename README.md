# Raw Material Optimization

## Overview

This project uses **Linear Programming (LP)** to optimize the selection and quantity of raw materials for a protein bar recipe. The goal is to **minimize total ingredient cost** while meeting specific nutritional requirements.

The optimization is implemented in Python using the **PuLP** library, leveraging nutritional composition and cost data for different ingredients.

---

## Features

* **Data Import and Cleaning**
  Reads nutritional and cost data from Excel files and preprocesses them for analysis.

* **Decision Variables**
  Determines the optimal quantity of each ingredient.

* **Objective Function**
  Minimizes the total cost of ingredients.

* **Nutritional Constraints**:

  * Total weight must be exactly 150g
  * Protein content ≥ 22g
  * Fat content ≤ 20g
  * Fibre content ≥ 6g
  * Salt content ≤ 3g
  * Sugar content ≤ 20g

---

## Requirements

* **Python** 3.x

* **Required libraries**:

  ```bash
  pip install pulp pandas openpyxl
  ```

* **Input files**:

  * `Nutrition Facts.xlsx`: Contains nutritional composition per ingredient.
  * `Costs.xlsx`: Contains cost per ingredient.

---

## How It Works

### 1. Data Loading

Nutritional and cost data are loaded from Excel sheets and cleaned by removing unnecessary columns and missing values.

### 2. Model Definition

The LP model is created with decision variables representing the quantity of each ingredient.

### 3. Objective Function

Minimize:

$$
\text{Total Cost} = \sum (\text{Cost per ingredient} \times \text{Quantity})
$$

### 4. Constraints

Applied based on nutritional guidelines and recipe requirements.

### 5. Optimization

The PuLP solver finds the ingredient combination that satisfies constraints at the lowest cost.

---

## Example Ingredients

* Chicken
* Beef
* Mutton
* Rice
* Wheat bran
* Corn
* Peanuts

---

## Running the Project

1. Ensure `Nutrition Facts.xlsx` and `Costs.xlsx` are in the same directory as the notebook.
2. Open and run `Raw Material Optimization.ipynb` in Jupyter Notebook or JupyterLab.
3. The model output will display:

   * Optimal ingredient quantities
   * Total cost
   * Constraint satisfaction check

---

## Applications

* Food manufacturing cost optimization
* Recipe formulation under dietary constraints
* Supply chain and procurement planning for raw materials

