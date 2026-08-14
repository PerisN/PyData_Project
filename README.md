## Analyzing Growth Velocity, Market Shifts and Transaction Patterns Across Kenya’s Mobile Money Sector.

---

## Project Description.
Kenya is recognized globally as a leader in mobile money and digital financial inclusion. While Safaricom's M-Pesa historically led the market, competitor platforms such as Airtel Money, Telkom T-kash, Equitel and bank-backed wallets like NCBA Loop and Absa Timiza have captured growing market share by allowing citizens to deposit, transfer and withdraw money using mobile phones.

 However, digital adoption is not static, it shifts over time due to economic factors, seasonal spending cycles, policy changes and physical agent network expansion. Digital finance in Kenya is no longer a single-provider story. 

This project deliberately focuses on a Macroeconomics Sector Analysis, it analyzes national-level monthly data from the Central Bank of Kenya (CBK) to evaluate the entire ecosystem of mobile wallets. It tracks how total account registrations, active cash-in/cash-out agent networks, total transaction counts and total monetary value ($KSh\ billions$) have expanded and fluctuated over time.

In short, My project looks at Kenya's mobile money system over time to see how people actually spend money, when the busiest months are and if there are enough agents to help everyone.

---

## Problem Statement.
Many policy makers, fintech managers and economic analysts evaluate digital financial inclusion using static headline metrics like total registered accounts. However, relying solely on registration numbers creates two critical analytical blind spots:

> - Active Usage vs. Dormant Accounts: A high number of registered accounts does not guarantee continuous economic utility if transaction velocity fluctuates heavily or drops off.

> - Network Capacity and Liquidity Risks: As user onboarding scales across mobile money networks, the supporting agent infrastructure faces operational pressure. Without evaluating agent density against transaction velocity, networks risk severe cash liquidity bottlenecks, particularly during peak spending seasons.

To address these limitations, this project converts raw, monthly Central Bank of Kenya (CBK) time-series data into an interactive Python analytics pipeline. By modeling growth velocity, calculating agent-to-user ratios and identifying seasonal liquidity cycles, it provides data-driven insights into Kenya’s digital payments infrastructure.

--- 

## Project Objective.
1. National Data Cleaning and Resampling (Pandas).
> - Clean, format, and structure the raw CBK monthly payment dataset.
> - Combine Year and Month string columns into a unified DatetimeIndex in Pandas to enable seamless temporal resampling and rolling calculations.

2. Agent Network Efficiency & Basket Size Math (NumPy).
Calculate national-level indicators over time:
> - User-to-Agent Density Ratio: Total National Mobile Accounts/Total Active Agent Out.
> - National Average Basket Size: Total Value Moved (KSh) / Total Transaction Count.

3. Industrial Seasonality & Volatility Mapping (Seaborn).
> - Cyclical Payment Heatmaps: Construct multi-year Seaborn heatmaps to identify recurring monthly transaction spikes and spending contractions.
> - Liquidity Variance Analysis: Measure month-over-month (MoM) volatility in payment values (KSh\ Billions) to highlight seasonal liquidity strain—contrasting high-volume periods (e.g., December holiday retail and January school fee payments) against post-holiday usage pullbacks.

4. Statistical Visualization & Dashboarding (Matplotlib)
Assemble a publication-ready, 4-panel visual dashboard summarizing key macro trends:
> - Transaction Volume and Value: Dual-axis time-series tracking overall throughput in KSh\ Billions alongside total monthly transaction counts.
> - Network Scale Trends: Comparative trajectory plotting the expansion of Active Agent Outlets against Total Registered Accounts.
> - Average Basket Size: Historical trendline tracking the average value per individual transaction (KSh) over time.
> - Monthly Seasonality Heatmap: Pivot-table visual matrix displaying monthly payment intensity across calendar years.


---

## Research Questions
A. Ecosystem Expansion & Network Capacity (Pandas and NumPy)
Focuses on macro growth velocity and whether the physical agent infrastructure is keeping up with user onboarding.

> - What is the long-term Compound Annual Growth Rate (CAGR) of total registered mobile money accounts compared to physical active agents across Kenya's digital wallet sector?!

> - How has the User-to-Agent Density Ratio (Total Accounts / Active Agents) evolved over time, and does the data signal physical agent network saturation?

> - How has the Average Basket Size (Total Value in KSh / Total Transaction Volume) shifted over time, and is transaction value expanding faster than transaction count?

B. Industry Seasonality & Liquidity Volatility (Seaborn)
Focuses on cyclical payment patterns, month-over-month shifts, and seasonal liquidity demand spikes.

> - Which calendar months consistently exhibit peak transaction volumes and values across different years?! 

> - How volatile are month-over-month (MoM) percentage changes in national transaction values (KSh\ Billions), and during which historical periods did the sector experience its sharpest swings?!

C. Long-Term Velocity & Macro Shifts (Matplotlib)
Focuses on rolling trendlines and correlations between ecosystem infrastructure variables.

> - What do 3-month and 12-month rolling averages reveal about the underlying long-term growth trajectory of Kenya's mobile payments throughput?!

> - How strongly correlated are active agent counts with overall transaction volume, and does expanding agent access directly correlate with higher transaction frequency?!

---

## Tech Stack and Libraries.
> - Pandas
> - NumPy
> - Seaborn
> - Matplotlib

---

## Dataset Sources.
Kaggle - https://www.kaggle.com/datasets/collinsogombo/kenyas-mobile-money-payments-data?select=Mobile+Payments.csv

Key Columns:-
> - Year
> - Month
> - Active Agents
> - Total Registered Mobile Money Accounts (Millions)
> - Total Agent Cash in Cash Out (Volume Million)
> - Total Agent Cash in Cash Out (Value KSh billions)

---

## Key Methodology and Pipeline.
1. Data Ingestion and Schema Auditing - Load the Central Bank of Kenya (CBK) time-series CSV file.
2. Preprocessing and Time-Series Structuring - Clean raw strings and convert the flat dataset into a structured time-series object.
3. Feature Engineering and Derived Metrics - Construct custom mathematical ratios to reveal operational realities behind the numbers.
4. Seasonality and Volatility Modeling - Evaluate monthly cash flow cycles and structural variance.
5. Visual Dashboard Assembly - Synthesize outputs into an executive 4-panel visual dashboard.
