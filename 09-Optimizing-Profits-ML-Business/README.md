# Optimizing Profits for OilyGiant using ML Business Metrics

Short description:

The OilyGiant mining company is looking to expand its operations by drilling new oil wells in one of three regions. comprehensive data science project has been initiated. The primary goal of this project is to select the region that will maximize profit for the company.

# Data description

Geological exploration data for the three regions are stored in files:

    geo_data_0.csv
    geo_data_1.csv
    geo_data_2.csv
    id — unique oil well identifier
    f0, f1, f2 — three features of points
    product — volume of reserves in the oil well (thousand barrels).

# Conditions:

Only linear regression is suitable for model training (the rest are not sufficiently predictable).
When exploring the region, a study of 500 points is carried with picking the best 200 points for the profit calculation.

The budget for development of 200 oil wells is 100 USD million.
One barrel of raw materials brings 4.5 USD of revenue The revenue from one unit of product is 4,500 dollars (volume of reserves is in thousand barrels).

After the risk evaluation, keep only the regions with the risk of losses lower than 2.5%. From the ones that fit the criteria, the region with the highest average profit should be selected.

# Results

After conducting a thorough analysis of the three regions for potential oil well development, the following key findings have been observed.

Based on the calculated profits for each region, it is evident that Region 1 stands out as the most financially promising choice for oil well development. Region 1 not only surpasses the other two regions in potential returns but also carries the lowest risk of incurring losses.

Considering both profitability and risk mitigation, it is strongly recommended to prioritize the development of oil wells in Region 1. This region demonstrates the highest profit potential and is the most favorable option for optimizing returns on investment.

While the profit calculations provide valuable insights, it is important to note that other critical factors such as geological assessments, environmental considerations, and operational feasibility should be thoroughly evaluated before proceeding with drilling activities. Nonetheless, the financial analysis strongly supports Region 0 as the preferred choice for new oil well development.
