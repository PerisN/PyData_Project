## Analyzing Kenya's Mobile Money Growth and Transaction Volatility.

---

## Project Description.
Kenya is recognized globally as a leader in mobile money and digital financial inclusion. Platforms like M-Pesa and Airtel Money transformed the economy by allowing citizens to deposit, transfer and withdraw money using mobile phones. However, digital adoption is not static, it shifts over time due to economic factors, seasonal spending, policy changes and agent network expansion.

This project is a time-series data analysis project that explores the evolution of digital finance in Kenya using official Central Bank monthly data.

Instead of treating financial inclusion as a simple headline number e.g., x million users registered, this project analyzes how money actually flows through the system over time. This project breaks down, how fast the customer base and agent support networks have grown, how transaction volumes (number of payments) and transaction values (billion Ksh moved) behave month to month and where spikes and liquididty strains occur (such as holiday spending peaks vs. post-holiday contractions).

---

## Problem Statement.
Many policy makers, fintech managers and economic analysts evaluate digital financial inclusion using flat, single-point metrics such as total registered users. This creates two major analytical blind spots: 

> - Active Usage vs. Dormant Accounts: A high number of registered accounts does not guarantee continuous economic utility if transaction velocity fluctuates heavily or drops off.
> - Network Saturation & Liquidity Risks: As millions of users join mobile money networks, the physical agent network (cash-in/cash-out points) faces severe pressure. Without tracking agent density against transaction volumes, financial networks risk liquidity bottlenecks, especially during peak spending months.

This project transforms static monthly CBK records into an interactive Python analytics pipeline. It calculates growth velocity, evaluates agent-to-user ratios and identifies seasonal spending cycles to provide actionable data on Kenya’s digital payments infrastructure.


--- 

## Project Objective.
1. Data wrangling and time-series preparation (Pandas)
> - Clean, format, and structure the raw CBK monthly payment dataset.
> - Combine Year and Month string columns into a unified DatetimeIndex in Pandas to enable seamless temporal resampling and rolling calculations.

2. Network growth and ratio analysis (Pandas & NumPy).

Compute key structural ratios over time, including:
> - Agent Density: Average number of active registered accounts served per physical agent outlet.
> - Average Basket Size: Average value per transaction (Total KSh Value / Total Transaction Volume.
Calculate Compound Annual Growth Rates (CAGR) and Year-over-Year (YoY) percentage changes for overall network expansion.

3. Seasonality & Volatility Evaluation (Seaborn).
> - Identify recurring monthly transaction patterns using Seaborn heatmaps and distribution plots.
> - Determine which specific months experience the highest variance in liquidity demand (e.g., December spending vs. January/February drop-offs).

4. Statistical Visualization & Dashboarding (Matplotlib)

Build a 4-panel executive visual dashboard summarizing:
> - Total Transaction Value ($KSh\ Billions$) over time
> - Active Agents vs. Registered Accounts growth trendlines.
> - Average Transaction Size ($KSh$) over time.
> - Monthly seasonality heatmap.


---

## Research Questions
A. Adoption & Network Expansion (Pandas and NumPy).
Focuses on how fast the mobile money ecosystem is expanding and whether infrastructure is keeping pace with user onboarding.
> - 1. How has the ratio of active accounts per agent evolved, and is agent growth keeping pace with account registrations?!
> - 2. What are the compound annual growth rates (CAGR) of total registered mobile money accounts versus active agent outlets over the dataset's timeframe?!

B. Seasonality, liquidity and volatility (Seaborn).
Focuses on identifying cyclical spending behavior and months with high liquidity demands.
> - 3. Which calendar months consistently exhibit peak transaction volumes and value spikes?!
> - 4. How volatile are month-over-month (MoM) percentage changes in total transaction values, and during which historical periods did mobile money experience its highest volatility spikes?

C. Long-Term Trends & Structural Shifts (Matplotlib)
Focuses on macro-level shifts and milestone changes in Kenya's digital financial landscape.
> - 5. What are the 3-month and 12-month rolling averages for total monthly transaction value ($KSh\ billions$) and what do they reveal about the underlying long-term growth trajectory?!
> - 6. How strongly correlated are active agent counts with overall transaction volume and does an increase in physical agents directly drive higher transaction frequency?

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
> - Pandas Data Transformation - combine year plus month into pd.DatetimeIndex and strip string formatting and handle NaNs.
> - NumPy Feature Engineering - Calculate Avg Value per Txn = (Value / Volume) and Calculate YoY % Growth & Rolling Averages.
> - Seaborn Statistical Plots - Monthly Heatmap (Year vs Month) and Regression/Trendline (Agents vs Accounts).
> - Matplotlib Dashboard - Export 4-panel executive chart.
