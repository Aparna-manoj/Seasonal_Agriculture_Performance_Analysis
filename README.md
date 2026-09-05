# Seasonal_Agriculture_Performance_Analysis
A data analytics project analyzing seasonal agricultural performance across crops, states, and seasons using Python - covering data cleaning, statistical testing, and profitability analysis.

## The Data Set

- Source file: seasonalagricultureperformance_dataset.csv
- Number of records: 4,000. Number of attributes: 28
- Seasons in record: Kharif, Rabi, Zaid
- Crops recorded: Rice, Wheat, Maize, Pulses, Cotton, Chili, Ground-nuts, Sugarcane
- Important fields: rainfall, temperature,soil conditions,water irrigation types, amounts applied of fertilizers and water, output, yield, production, revenue generated, cost- to-produce and profit. The profit margin as well as the water use efficiencies and the danger index on disease and pests for any given crop season is also calculated and recorded

## Objectives
 
- Clean and prepare the dataset for reliable analysis
- Compare agricultural performance across seasons and crops
- Analyze financial outcomes: revenue, cost, profit, and profit margin
- Study water usage efficiency and irrigation methods
- Test whether observed seasonal/crop differences are statistically significant
- Turn the findings into practical, evidence-based recommendations

  ## Methodology

1. **Data Cleaning:** Missing values in Rainfall, Soil Moisture, and Yield were imputed using season-wise and crop+season-wise medians. An indicator flag was created to track which yield values were imputed, keeping the process transparent and traceable.
2. **Exploratory Data Analysis:** Yield, revenue, cost, and profit were examined across seasons, crops, and crop-season combinations, supported by visualizations.
3. **Statistical Testing:** Kruskal-Wallis and Mann-Whitney U tests (with Bonferroni correction) were used to check whether seasonal differences in yield, profit, and water efficiency are statistically significant. Spearman correlation was used to examine the relationship between disease/pest risk and profit.
4. **Validation:** All financial and production formulas (Profit = Revenue − Cost, Production = Farm Area × Yield, etc.) were independently verified against the raw dataset.

## Key Findings

- **Best season overall:** Kharif — highest average profit and water efficiency
- **Weakest season:** Zaid — lowest average profit and water efficiency
- **Most profitable crops:** Sugarcane and Chilli, which stay profitable across all three seasons
- **Weakest crops:** Rice, Wheat, and Maize show negative profit margins in most seasons, worsening further in Zaid
- **Irrigation matters:** Drip irrigation shows the highest average yield; Rainfed the lowest
- Seasonal differences in yield, profit, and water efficiency are statistically significant (p < 0.001)
- Disease/pest risk has a statistically significant but practically weak relationship with profit (Spearman correlation ≈ 0.10)

## Recommendations

- Prioritize Kharif season and high-margin crops like Sugarcane and Chilli
- Review or reconsider Rice, Wheat, and Maize cultivation in Zaid due to consistent losses
- Choose irrigation methods carefully, as they meaningfully affect yield
- Monitor water usage and disease/pest risk more closely to protect profitability
- Base crop and season planning on both profitability and resource efficiency, not yield alone

## Tools Used

- Python (pandas, numpy, matplotlib, seaborn, scipy)
- Jupyter Notebook

## Files in this Repository

- `Seasonal_Agriculture_Performance_Analysis_FINAL (2).ipynb` — full analysis notebook
- `seasonal_agriculture_performance_dataset.csv` — dataset used for the analysis
- `VOIS_Major_Project_PPT.pptx` — final presentation slides
- `Major Project_Seasonal Agriculture Performance Analysis.pdf` — original project brief
