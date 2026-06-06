# Mumbai Cafe Business Dashboard

This project presents an Excel-based Business Dashboard built using a dataset of cafes across Mumbai. The dashboard explores customer ratings, review activity, cafe categories, and estimated business performance through interactive visualizations and KPI tracking.

The original dataset contains cafe information such as location, ratings, addresses, latitude, and longitude. To extend the analytical scope of the project, additional business-oriented metrics were engineered, allowing the dataset to be explored from a revenue and popularity perspective.

The dashboard includes KPI cards, Pivot Tables, Pivot Charts, Slicers, Scatter Plot Analysis, and geographic visualization using latitude and longitude data. The objective was to transform raw cafe information into a clean and interactive dashboard that supports quick business insights and exploratory analysis.

## Dashboard Features

* Total Cafes KPI
* Average Rating KPI
* Total Reviews KPI
* Estimated Revenue KPI
* Average Customer Rating by Area
* Top Revenue Generating Areas
* Top Cafes by Popularity Score
* Cafe Category Distribution
* Popularity vs Customer Satisfaction Scatter Plot
* Interactive Slicers for Area and Cafe Category

## Dashboard Preview

### Business Intelligence Dashboard

![Dashboard](images/dashboard.png)

### Mumbai Map Visualization

![Mumbai Map](images/mumbai-map.png)

### Working Dataset

![Dataset](images/working-dataset.png)

## Engineered Metrics & Formulas

### Popularity Score

Measures overall cafe popularity by combining customer rating and review volume.

**Formula:** Popularity Score = Rating × Total Ratings

### Estimated Monthly Visitors

Approximates monthly customer footfall using review activity.

**Formula:** Estimated Monthly Visitors = Total Ratings × 25

### Average Spend

Assigned based on cafe positioning and rating bands.

**Formula:**
* Rating ≥ 4.7 → ₹550
* Rating ≥ 4.4 → ₹450
* Rating ≥ 4.0 → ₹350
* Rating < 4.0 → ₹250

Excel Formula:

```excel
=IF(C2>=4.7,550,IF(C2>=4.4,450,IF(C2>=4,350,250)))
```

### Estimated Revenue

Calculated using estimated visitors and average spend.

**Formula:** Estimated Revenue = Estimated Monthly Visitors × Average Spend

Excel Formula:

```excel
=I2*J2
```

## Note

The columns **Estimated Monthly Visitors**, **Average Spend**, **Popularity Score**, and **Estimated Revenue** are synthetic metrics created solely for analytical and visualization purposes. They do not represent actual business figures and were generated to demonstrate dashboarding, KPI creation, and business analysis techniques.

## Dataset

Original dataset source:

https://www.kaggle.com/datasets/superveer70/mumbai-cafes-datasets/data

## License

This project is released under the MIT License.

## Author

**Tanuja Modak**

