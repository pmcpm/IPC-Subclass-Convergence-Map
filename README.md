# Global Overlay Map Data (IPC Subclass Level)

This repository contains the supplementary dataset for the research paper:
**"Global Overlay Map Based on DOCDB IPC Data for Visualizing Technological Convergence"**

While the main analysis in the paper focuses on the IPC Class level, this dataset provides fine-grained technological convergence networks and overlay maps at the **IPC Subclass (e.g., G06N)** level. These files are formatted for direct use with [VOSviewer](https://www.vosviewer.com/).

## 📂 Repository Structure

The dataset is organized as follows:

### 1. Root Directory (Raw Network Data)
Contains the raw co-occurrence edge lists for IPC Subclasses.

* **`Result_ipc_subClass_co_occurrence_20250329.csv`**
    * **Description**: The complete raw co-occurrence network of IPC Subclasses extracted from the DOCDB database.
    * **Format**: Likely `Source`, `Target`, `Co_occurrence frequency`.
* **`Result_ipc_subClass_keep2025_co_occurrence_20250329.csv`**
    * **Description**: The co-occurrence network filtered to include only IPC codes present in the **2025 version** of the IPC scheme (consistent with the paper's methodology).

### 2. `overlayMapFile/` Directory (VOSviewer Visualization Files)
Contains processed files ready for VOSviewer visualization (Base Maps and Overlay Scores).

#### Base Map Files (VOSviewer Map Files)
These files define the layout (coordinates), clustering, and labels of the global technology base map.

* **`Result_ipc_subClass_co_occurrence_20250329_frac_r0_5_min_50_map_keep2025IPC.csv`**
    * **Purpose**: Base map for a specific time window or subset.
    * **Parameters**: Fractional counting (`frac`), Resolution 0.5 (`r0_5`), Minimum occurence 50 (`min_50`).
* **`Result_ipc_subClass_co_occurrence_20250329_frac_r0_5_min_50_mapAllYear_keep2025IPC.csv`**
    * **Purpose**: **The Global Base Map**. Constructed using data from all years to ensure a stable structure for overlaying.
* **`Result_ipc_subClass_co_occurrence_20250329_frac_A2_R1_r1_min_20_map_keep2025IPC.csv`**
    * **Purpose**: Alternative map with different clustering/layout parameters (e.g., Resolution 1.0, Min occurence 20).

#### Overlay/Metric Files (VOSviewer Score Files)
These files contain the calculated convergence metrics to be overlaid on the base map.

* **`Result_ipc_subClass_co_occurrence_20250329_frac_r0_5_min_50_mapAllYear_keep2025IPC_weight_score.csv`**
    * **Purpose**: Contains the calculated node weights and scores corresponding to the base map.
* **`Result_ipc_subClass_co_occurrence_20250329_frac_A2_R1_r1_min_20_mapAllYear_keep2025IPC_weight_score.csv`**
    * **Purpose**: Contains the weights and scores corresponding to the alternative "A2_R1..." map.
