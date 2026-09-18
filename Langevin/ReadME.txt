# Langevin Dataset

This directory contains the Langevin instances and their corresponding arc-specific speed bound matrices used in our computational experiments.

## Folder Structure

* **Instances**: Contains the base vehicle routing instances, detailing customer coordinates, demands, service times, and time windows.
* **Maximum_speed**: Contains the upper bound (maximum) speed matrices. Each file is named `UB_matrix_[instance_name].txt` and corresponds to a specific base instance.
* **Minimum_speed**: Contains the lower bound (minimum) speed matrices. Each file is named `LB_matrix_[instance_name].txt` and corresponds to a specific base instance.

## Speed Matrix Data Format

For both the maximum and minimum speed folders:
* Each `.txt` file contains a square matrix corresponding to the nodes of that specific instance.
* The numerical value located at row `i` and column `j` represents the speed bound (upper or lower) on the directed arc from node `i` to node `j`.
* Values are formatted as standard floating-point numbers separated by tabs.
