# NBA Draft Analysis: Analyzing Key Determinants of Player Draft Outcomes

This project analyzes the key physical, performance, and experience factors that contribute to a US college basketball player being drafted into the NBA.

## Objectives & Hypothesis Testing

### 1. Physical Attributes (H1)
* **Research Question**: Are physical measurements (height, wingspan, weight, vertical leap) and athleticism associated with a higher draft position?
* **Hypothesis**: Taller players with wider wingspans and higher vertical leaps are drafted earlier.

### 2. College Performance (H2)
* **Research Question**: Which statistical metrics (points, rebounds, assists, blocks, shooting percentages, etc.) have the strongest influence on draft positions?
* **Hypothesis**: Players with more dominant offensive and defensive box-score statistics are drafted earlier.

### 3. College Experience vs. Upside (H3)
* **Research Question**: Do younger players or prospects with fewer college seasons get prioritized in the draft?
* **Hypothesis**: Players entering the draft with fewer college seasons are drafted earlier, as teams value youth and upside over experience.

---

## Methodology & Dataset

We utilize combined dataset records matching college career statistics (2009-2022) with NBA Draft Combine anthropometrics and physical test results.

* **Target Variables**:
  - Binary: `drafted` vs. `undrafted` ($1/0$)
  - Discrete: `pick` ($1-60$)
  - Categorical Hierarchy: `Lottery_Round_1` < `Non-Lottery_Round_1` < `Round_2` < `Undrafted`

* **Statistical Tests & Tools**:
  - **Independent T-tests**: Comparing physical and performance attributes of drafted vs. undrafted players.
  - **One-way ANOVA**: Assessing variance across the four draft tier groupings.
  - **Correlation Heatmaps**: Investigating exact relationships with specific draft pick numbers.
  - **Visualizations**: Multi-panel scatter plots with trend lines and distribution boxplots.

---

## Requirements & Setup

Ensure you have the following libraries installed to run the analysis:
```python
import pandas as pd
import numpy as np
from scipy import stats
import matplotlib.pyplot as plt
import seaborn as sns