# pyspark-brainwash-detection
# Brainwash Detection with PySpark (Distributed Database Management)

This project applies **PySpark** to large-scale TV viewership data, framed in a fun storyline where the Powerpuff Girls fight Mojo Jojo’s brainwashing.  
It was developed as part of the **Distributed Database Management** course (096224) at Technion.

## Part 1 — Brainwash Detection
- Detected malicious TV program titles based on 7 anomaly conditions:
  1. Above-average duration  
  2. Viewed by Toyota households  
  3. Viewed by households with 2 close-aged adults  
  4. Aired on Friday the 13th  
  5. Viewed by low-income households with >3 devices  
  6. Belonging to suspicious genres (Collectibles, Art, etc.)  
  7. Title contains suspicious words (e.g., “better”, “girls”, “call”, “the”)  
- Flagged malicious records; marked programs malicious if >40% of their airings were malicious.  
- Produced the **top-20 malicious titles**.

## Part 2 — Un-brainwashing
- Identified broadcast slots most effective for reversing brainwashing:
  - **Top 5 genres** (by household size viewers)  
  - **Top 5 DMAs** (by device count + household population)  
  - **Top 5 programs** (by households with children)  
- Calculated **DMA wealth score** = normalized average of income + net worth.  
- Assigned **11 unique genres** to the 10 wealthiest DMAs via sequential allocation.

## Deliverables
- `project1_part1.ipynb` — PySpark code for brainwash detection  
- `project1_part2.ipynb` — PySpark code for un-brainwashing strategy  

## Tools
- PySpark 3+ (Databricks)  
- Python 3.10  
- Libraries: `pyspark.sql`, `pandas`  
