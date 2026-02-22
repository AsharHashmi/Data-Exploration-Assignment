Walmart Temperature and Sales Analysis

What This Project Is About
I wanted to find out if hotter weather actually changes how much people spend at Walmart. Since temperatures have been rising over time, Walmart was curious whether higher temperatures might affect sales.

So the main question I tried to answer is:

Do higher temperatures causally affect sales?

The Data
I used weekly information from 45 different Walmart stores. The data runs from February 2010 through October 2012. For each store and week, I had:

- Weekly sales  
- Temperature  
- Whether it was a holiday week  
- Fuel prices  
- CPI (consumer price index)  
- Unemployment rate  

How I Went About It
This project was not as simple as just comparing hot weeks to cold weeks. The problem is that both temperature and sales follow the seasons. If we just look at the raw numbers, it can be misleading.

So I used a method that compares each store to itself over time, while also removing national weekly patterns (like seasonal shopping spikes) using date fixed effects. I also checked a few different versions of the model to make sure the results were robust:

- I tried it without any extra controls  
- I added a squared term to see if the relationship is nonlinear  
- I checked whether last week’s temperature matters for this week’s sales  
- I added store-specific trends to account for different long-run growth patterns across stores  

Files in This Folder
1) `Walmart Analysis.qmd` – Main Quarto file with all code  
2) `Walmart-Analysis.pdf` – Final write-up with results and explanations  
3) `data/Walmart_Sales.csv` – Original data  

If You Want to Run It Yourself
Open the .qmd` file in RStudio, make sure you have the packages installed (tidyverse, lubridate, fixest, modelsummary, etc.), and click Render.

What I Found
The short answer is: yes, temperature affects sales, but the effect is small.

In the main model, a one degree Fahrenheit increase in temperature is associated with about a 0.2% increase in weekly sales. So if it’s 10°F warmer in one week compared to another, that corresponds to about a 2% increase in sales. The effect is statistically detectable, but its economic magnitude is modest. Holiday spikes are absorbed by the Date fixed effects, and visually they appear much larger than the temperature effect.

Author: Ashar Hashmi  
Course: Applied Econometrics ECON-5300  
Date: 2/21/2026  