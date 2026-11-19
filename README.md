# Automobile Market & Price Analysis (`automobile.csv`)

**This project is made as part of a data anlysis portfolio**

An end-to-end data analysis and baseline predictive modeling project built on the UCI Automobile dataset (`automobile.csv`). The project follows a structured five-step workflow to uncover what drives vehicle pricing, examine performance vs. fuel-economy trade-offs, and establish a baseline price-prediction model.

---

## Project Structure & Methodology

1. **Business Understanding:** Defined core analytical questions around vehicle pricing drivers, brand and drivetrain positioning, fuel efficiency trade-offs, and price predictability.
2. **Data Cleaning:** Converted text-encoded numbers and string-formatted numeric columns (including handling `?` placeholders and missing values), verified data types, and inspected outliers using the Interquartile Range (IQR) method (`df_clean`).
3. **Exploratory Data Analysis (EDA):** Analyzed price distributions, correlation patterns across numerical features, horsepower vs. price relationships, and average pricing across manufacturers.
4. **Advanced Analysis:** Investigated pricing and performance differences across drivetrains (`drive_wheels`), fuel types (`fuel_type`), and body styles (`body_style`).
5. **Predictive Modeling (ML):** Built and evaluated a baseline **Linear Regression** model (`80/20` train-test split) using key technical and dimensional features (`horsepower`, `curb_weight`, `engine_size`, `highway_mpg`, `width`) to predict `price`, evaluated via **$R^2$** and **RMSE**.

---

## Key Conclusions

* **Size, Weight, and Power Drive Pricing:** Vehicle mass (`curb_weight`), width (`width`), and engine displacement (`engine_size`)—alongside `horsepower`—are primary numerical drivers of automobile price, with heavier, larger, and higher-power cars generally commanding higher prices.
* **Performance vs. Fuel Economy Trade-Off:** Higher power and vehicle weight align with lower fuel efficiency (`city_mpg` and `highway_mpg`), highlighting a clear trade-off between performance/size and operating fuel economy.
* **Clear Market Tiering:** Luxury manufacturers (such as Jaguar, Mercedes-Benz, Porsche, and BMW), rear-wheel drive (`rwd`) configurations, and specialty body styles occupy higher price tiers, whereas standard `fwd` vehicles cluster in more budget-friendly ranges.
* **Baseline Predictive Capability:** A linear regression baseline on core technical specs captures a meaningful share of price variance, while larger prediction errors on higher-priced cars point to non-linear dynamics and unmodeled brand/trim effects.

---

## Recommendations & Next Steps

* **Pricing & Benchmarking:** Benchmark vehicles against peer models using technical specifications (`curb_weight`, `engine_size`, `horsepower`, `highway_mpg`) while accounting for brand equity in luxury segments.
* **Product & Segment Alignment:** Balance engine output and vehicle scale with fuel economy targets (`city_mpg` / `highway_mpg`) when positioning vehicles for cost-conscious or commuter buyers.
* **Model Iteration:** Incorporate categorical variables (such as `make`, `body_style`, `fuel_type`, and `drive_wheels`) via encoding and evaluate non-linear models (such as **Random Forest** or **Gradient Boosting**) to improve accuracy at upper price tiers.

---

## Tech Stack & Setup

* **Language & Libraries:** Python, `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

Install dependencies and launch the notebook:

```bash
pip install -r requirements.txt
jupyter notebook