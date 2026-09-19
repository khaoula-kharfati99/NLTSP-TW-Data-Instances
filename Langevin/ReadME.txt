# Langevin Dataset

This directory contains the Langevin instances, the generated demand, and their corresponding arc-specific speed bound matrices used in our computational experiments.

## Folder Structure

* **Instances**: Contains the base instances, detailing node coordinates, service times, and time windows.
* **Demands**: Contains the generated demand vectors for the customers. Because the random seed was fixed during data generation, all instances with the same number of customers share the exact same demand vector. 
* **Maximum_speed**: Contains the upper bound (maximum) speed matrices. Each file is named `UB_matrix_[instance_name].txt` and corresponds to a specific base instance.
* **Minimum_speed**: Contains the lower bound (minimum) speed matrices. Each file is named `LB_matrix_[instance_name].txt` and corresponds to a specific base instance.

## Data Format Guidelines

### 1. Speed Matrices
For both the maximum and minimum speed `.txt` files. To ensure consistency with the base instance files:
* **0-Based Indexing:** The row and column indices start at 0. 
* **Node Alignment:** 
  * Row/Column 0 corresponds to the starting depot (ID 0).
  * Rows/Columns 1 through N correspond to the customer nodes (IDs 1 to N).
  * The final row/column corresponds to the copied ending depot.
* **Arc Mapping:** The numerical value located at row i and column j strictly represents the speed bound on the directed arc from node ID i to node ID j. 

### 2. Demand Files
Each `.txt` file in the **Demands** folder contains a single column of integer values representing the demands (q_i) for that instance class. 
* The first line is 0 (the starting depot).
* The intermediate lines represent the customer demands.
* The final line is 0 (the copied ending depot). 

