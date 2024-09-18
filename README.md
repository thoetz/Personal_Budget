# Personal_Budget
A user-friendly Google Sheets tool that helps individuals track their income, expenses, savings, and taxes.

Create a copy and try it out for yourself!

## [Budget Calculator Dashboard](https://docs.google.com/spreadsheets/d/1FtAMYj3UdYxYSYJcn3afPHnDjG8OAJMkfgP50WmLcOU/edit?usp=sharing)


### Project Overview
Created a budget calculator that is easy to use and helps people keep track of their spending and map out their income, savings, and expenses on a monthly or yearly basis.

### Considering My Audience
The audience I considered was younger individuals who are just beginning to live on their own or looking to start saving to plan for the future. I also focused on making the dashboard aesthetically pleasing and user-friendly so that individuals who are not too technical could navigate the dashboard easily and find it intuitive and useful.

### Keeping it Simple and Focused
I ensured my dashboard was simple, easy to read, and focused on budgeting and personal finance. I included a savings interest projection to show how compound interest can grow their savings. I also integrated a tax calculator to demonstrate how taxes work in different income tiers and how contributions to RRSP or FHSA can reduce taxable income.

### My Process
**Planning and Design:**  
Once I identified the elements to include in the dashboard, I sketched a layout on paper. This helped ensure logical flow and avoid overcrowding the space with too much information.

### Building the Model

#### Income Section
The income section allows the user to input weekly hours worked and an hourly wage to calculate approximate monthly earnings.  
*Technical Explanation:* Utilized basic multiplication formulas to calculate monthly earnings based on user inputs.

#### Savings Calculator
The savings calculator uses a percentage input to calculate monthly savings. I added conditional formatting to alert the user if the savings rate is not between 1% and 100%.
*Technical Explanation:* Applied conditional formatting and basic arithmetic to calculate savings based on user inputs.

#### Expenses Section
Users can input recurring expenses as either monthly, yearly, or weekly amounts. Each expense can be categorized as a "Want" or "Need" for better financial visibility. Data validation was applied to ensure accuracy in the frequency and category columns.  
*Technical Explanation:* Used `ARRAYFORMULA` and an `IF` statement to adjust yearly, monthly, or weekly amounts dynamically.

#### Spending Breakdown
A chart visualizes how the user's income is being spent, including savings and a further breakdown of expenses into "Wants," "Needs," and "Debt."
*Technical Explanation:* Used dynamic charting based on categorized expenses and conditional formatting for visual representation.

### Key Values
I added key value cards to provide a quick summary of Income, Expenses, Savings, and Extra Cash. These values could be toggled between yearly and monthly views using data validation and `IF` formulas.

### Affordability Calculator
The affordability calculator shows what users can afford based on their current income, following the 70/20/10 budgeting rule (70% needs, 20% wants, 10% savings). If the need exceeds 70% of the income, the calculator generates an alert.
*Technical Explanation:* Used concatenation and `IF` statements to validate and display whether spending exceeded recommended thresholds.

### Savings Projection
A time series graph projects how savings will grow over time. Users input their initial investment, monthly contributions, interest rate, and investment duration. The graph updates dynamically based on selected periods (5, 10, 15, 25, or 30 years).  
*Technical Explanation:* Utilized the `FILTER` function to create a dynamic table based on user inputs, updating the graph accordingly. Also added optimistic and pessimistic projections by adjusting the interest rate by ±1%.

### Tax Calculator
I built a tax calculator for Albertan residents, with room to adapt for other provinces. It applies progressive tax rates from the Canadian federal tax table.
*Technical Explanation:* Nested `IF` statements applied progressive tax rates based on income.

### Tax Shield Calculation
This shows how RRSP contributions can lower taxable income and save money.  
*Technical Explanation:* Used arithmetic to subtract RRSP contributions from taxable income and recompute tax savings, using nested `IF` statements to adjust based on contributions.

### Visualizations
I added a pie chart to visualize the allocation of federal and provincial taxes along with the remaining income, helping users understand how their income is taxed.

