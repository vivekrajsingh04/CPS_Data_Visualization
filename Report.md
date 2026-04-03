# Data Visualization and Analytics using JMP

## 1. Introduction & Dataset Selection
This assignment focuses on the multifaceted layers of visual analytics, spanning down from fundamental design abstractions, to utilizing dashboards within tools equivalent to JMP, out toward emerging methodologies like Digital Twins and Augmented Reality. 

A **Customer Behavior and Restaurant Tipping Dataset** ("tips" dataset broadly matching standardized JMP Sample libraries and UCI formats) has been chosen for analysis. It contains data points regarding customer bills, tips, sex, day of week, meal time, and party sizes.

## 2. Data Abstraction
Data abstraction refers to simplifying and structurally classifying the dataset semantics prior to visual encoding:
- **Structural Mapping**: The dataset operates as a **Table** consisting of Items (individual diners or bills) mapped to specific Attributes.
- **Data Types Encountered**:
  - `total_bill` and `tip`: **Continuous / Quantitative** attributes representing currency.
  - `sex` and `time`: **Categorical / Nominal** variables indicating categories without implicit mathematical ranking.
  - `day`: **Ordinal** sequence classifying the chronological progression of the week.
  - `size`: **Quantitative Discrete** variable defining party count.

## 3. Task Abstraction
Task abstraction identifies what analytical goals we attempt to solve via Visualization mapping:
- **Goal #1 (Comparison & Distribution):** Compare the average total bills spent based on the day of the week, segmented by Gender demographics.
- **Goal #2 (Correlation Trends):** Analyze the linear relationship between the total bill amount and the tip given, observing if party size influences density.
- **Goal #3 (Density & Matrix Interrelation):** Identify global numerical dependencies through correlation heatmap indices.

## 4. Visualizations & Validating Labels
*Note: Due to automated environments, equivalent graphs adhering identically to JMP's graph builder standards were synthesized dynamically. Strict labeling validation methodologies have been applied directly to coordinates to remove ambiguity.*

### 4.1 Bar Chart (Categorical Comparisons)
**Validation applied**: The X-axis enumerates the Nominal categories accurately. The primary Y-axis explicitly specifies mathematical units `Average Total Bill ($)`. The legend accurately identifies color-to-gender grouping without overlap.

![Bar Chart](/Users/yash/Desktop/ASSIGNMENT CPS/bar_chart.png)

### 4.2 Scatter Plot (Trend Identifications)
**Validation applied**: Multi-variate plot where X and Y axes utilize continuous scales properly marked by units. Marker scale mappings `(sizes)` map visually to party size linearly assisting in depth interpretation, mapped via a dedicated boundary legend.

![Scatter Plot](/Users/yash/Desktop/ASSIGNMENT CPS/scatter_plot.png)

### 4.3 Heatmap (Density & Correlation Matrix)
**Validation applied**: A strict diverging color ramp (red for positive, blue for negative) surrounds a 0.0 baseline, ensuring perceptual accuracy. Data indices are directly annotated onto the cells yielding high precision lookup values.

![Heatmap](/Users/yash/Desktop/ASSIGNMENT CPS/heatmap.png)

## 5. Workflow Design
Developing analytics transitions through a generalized workflow pipeline:
1. **Data Collection & Integration:** Extracting raw data systematically through API pipelines, sensor queries, or manual CSV ingestion.
2. **Data Wrangling (Cleaning):** Processing nulls, fixing datatype parsing issues, and reshaping columns.
3. **Data & Task Abstraction Specification:** Identifying the types and the desired user analysis outputs.
4. **Visual Encoding Construction:** Passing processed frames into engines (like JMP's graph builder or Matplotlib) mapping data onto visual channels (e.g. position, hue, scale).
5. **Human Interpretation:** Reviewing results iteratively to locate actionable business insights, enabling rapid, informed decisions.

## 6. Emerging Concepts in Analytics

### 6.1 Augmented Reality (AR) in Visualization
**Augmented Reality (AR)** is the integration of digital, computer-generated visual components onto the real-world operational workspace.
- **Use in Visualization**: AR shifts data from 2D monitors into spatial 3D environments. This is particularly prevalent in architectural visualization and geospatial heatmapping (e.g., viewing localized population variances overlaid physically over the terrain). It enhances immersive exploration by permitting analysts to view 3D scatter topologies natively.

### 6.2 The Cyber Twin (Digital Twin) Concept
The **Cyber/Digital Twin** represents a completely synchronized digital counterpart to a physical entity, system, or process.
- **Explanation**: Through extensive IoT (Internet of Things) sensor networking, a physical machine continuously streams state-data to a virtual simulation. If engineers need to test stress limits or review historical performance optimizations, they interact with the Cyber Twin without risking physical degradation, enabling purely predictive maintenance.

### 6.3 Microsoft Power BI
**Power BI** represents a unified, scalable platform for cloud-native self-service enterprise business intelligence.
- **Cloud Integration**: It directly connects with massive cloud warehouses (Azure, AWS) querying real-time datasets.
- **Dashboards**: Rather than static plots, PowerBI excels at creating cohesive, highly-interactive Dashboards where executives can click particular geographic slices and watch interconnected bar charts update dynamically using dynamic DAX measures.

## 7. Results & Summarization Insights
From our generated distributions:
- **Correlations:** There is a well-defined positive correlation mapping total meal costs to tip amounts, predictably scaling with party sizes spanning denser clusters.
- **Comparisons:** Weekend sales distributions (Saturday/Sunday) eclipse weekday norms across total bills, emphasizing that dynamic staffing should peak appropriately during weekend rush-hours.

## 8. Conclusion
Visualizing raw datasets through established abstraction layers critically defines the narrative analysts can achieve. Frameworks like JMP simplify visual encoding, whereas adopting Digital Twins and AR topologies expands visualization beyond the constraints of two-dimensional mediums toward spatially-aware cognitive computing.
