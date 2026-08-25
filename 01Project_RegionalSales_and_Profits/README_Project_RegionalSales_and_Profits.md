# Regional Sales and Profits — Tableau Data Visualization Project

## Project Overview
This project is an interactive Tableau data visualization and exploratory analysis of <b>sales and profitability across U.S. regions, states, cities, product categories, and years from 2019 to 2022</b>.
The project was designed as a <b>progressive analytical story</b> rather than a collection of independent charts. The analysis begins with a broad comparison of regional sales and product performance, then progressively narrows the scope to a specific product sub-category, identifies underperforming states within the South region, drills down into North Carolina, and finally investigates city-level sources of machine-related profit losses.
The overall analytical path is:
<b>Regional Overview → Product-Level Analysis → Geographic Diagnosis → State-Level Drill-Down → City-Level Profit Investigation</b>
This structure allows the viewer to move from a high-level understanding of business performance toward increasingly specific questions about <b>where and why profitability is weak</b>.

##### Tableau Public
[View the interactive Regional Sales and Profits dashboard on Tableau Public](https://public.tableau.com/views/1RegionalSalesandProfits_16693535740520/ImproveProfitsintheSouth?:language=zh-CN&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)⁠
Note: The Tableau Public version is interactive. The GitHub repository documents the analytical structure, visualization design, and reasoning behind the dashboard, while Tableau Public provides the full interactive experience.

 
<div class='tableauPlaceholder' id='viz1784884316990' style='position: relative'><noscript><a href='#'><img alt='&lt;Story 1&gt; ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;1R&#47;1RegionalSalesandProfits_16693535740520&#47;ImproveProfitsintheSouth&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='1RegionalSalesandProfits_16693535740520&#47;ImproveProfitsintheSouth' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;1R&#47;1RegionalSalesandProfits_16693535740520&#47;ImproveProfitsintheSouth&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='zh-CN' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1784884316990');                    var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.width='1016px';vizElement.style.height='991px';                    var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>


⸻

 
## Analytical Objective
The central objective of the project is to explore the relationship between <b>sales volume and profitability</b> across multiple levels of geographic and product aggregation.
Rather than asking only:
Which products generate the most sales?
the visualization is designed to support broader questions such as:
* Which product sub-categories generate high sales but relatively weak profitability?
* How does sales performance vary across regions and years?
* Which states within the South region appear to underperform?
* Is North Carolina’s profitability consistent across years?
* Which product categories contribute to North Carolina’s performance?
* Can a state-level profitability problem be traced further down to individual cities and products?
* Where are machine-related profits being lost, and how large are the losses?
The dashboard therefore combines <b>descriptive visualization, comparative analysis, geographic exploration, temporal analysis, and hierarchical drill-down</b>.<br>
 
⸻


## Dataset
The visualization uses a sales and profitability dataset containing transactional/business performance information across U.S. geographic and product dimensions.
### Key dimensions
|Field|	Description|
|-----|------------|
|Region|	Geographic region: Central, East, South, West|
|State/Province|	U.S. state-level geographic information|
|City|	City-level geographic information|
|Category|	Product category|
|Sub-Category|Product sub-category|
|Order Date|	Order date, analyzed primarily at the year level|
|Sales|	Sales amount|
|Profit|	Profit amount|
|Profit Ratio|	Profitability ratio used in the geographic views|
The dataset covers four years: <b>2019, 2020, 2021, and 2022</b>
and four major regions: <b>Central, East, South, and West</b>
The product dimension contains multiple sub-categories, including:
* Accessories
* Appliances
* Art
* Binders
* Bookcases
* Chairs
* Copiers
* Envelopes
* Fasteners
* Furnishings
* Labels
* Machines
* Paper
* Phones
* Storage
* Supplies
* Tables
The project focuses particularly on the <b>South region, North Carolina</b>, and the <b>Machines</b> sub-category during the later stages of the analytical story.
 
⸻


## Visualization Design
A major design principle throughout the project is the simultaneous visualization of <b>Sales and Profit</b>.
For the primary bar charts:
* <b>Bar height → Sales</b>
* <b>Bar color → Profit</b>
This allows two related business dimensions to be examined simultaneously.
A product can therefore be evaluated not only by how much it sells, but also by whether those sales are associated with positive or negative profitability.
The profit color scale uses a diverging continuous encoding:
<b>negative profit → orange/red</b>
<b>positive profit → blue</b>
This is particularly useful for identifying situations where high sales do not necessarily correspond to high profitability.
### Interactive exploration
The dashboards incorporate interactive filters and Tableau tooltips to allow users to change the analytical scope.
Depending on the story point, users can explore:
* Region
* Year
* Product sub-category
* State
* City
Hovering over marks also exposes additional information such as:
* Category
* Region
* State/Province
* Sub-Category
* Order Date
* Sales
* Profit
* Profit Ratio where applicable
This design turns the visualization from a static report into an exploratory analytical interface.

⸻
 
## Story Structure
The Tableau workbook contains <b>9 story points</b>, organized as a progressive drill-down.
|Tab|	Story| Point|	Analytical| Purpose|
|---|------|------|-----------|--------|
|1|	Sales and Profit by Year|	Establish the overall regional and product-level performance|
|2|	Machine Sales by Year|	Isolate the Machines sub-category|
|3|	Underperforming Items in the South|	Identify geographic and product-level underperformance|
|4|	Profit in North Carolina, 2019–2022|	Drill down from the South region to North Carolina|
|5|	Profit in North Carolina, 2019|	Examine the 2019 state-level performance|
|6|	Profit in North Carolina, 2020|	Examine the 2020 state-level performance|
|7|	Profit in North Carolina, 2021|	Examine the 2021 state-level performance|
|8|	Profit in North Carolina, 2022|	Examine the 2022 state-level performance|
|9|	Where Are We Losing Machine Profits in North Carolina in 2022?|	Identify city/product-level sources of machine profit loss|
The sequence follows a <b>drill-down data story</b>: establish context first, identify an area of interest, and then progressively investigate the underlying dimensions. This is consistent with Tableau’s recommended use of story points to connect different views and support analytical narratives. 
 
⸻


## Tab 1 — Sales and Profit by Year

### Purpose
The first story point provides the broadest view of the analysis.
It compares <b>sales across product sub-categories and years</b>, while simultaneously encoding profitability through color.
### Visualization
The primary visualization is a grouped bar chart.
* <b>X-axis:</b> Order Date by Year → Sub-Category
* <b>Y-axis:</b> Sales
* <b>Color:</b> Profit
* <b>Filters:</b> Region, Sub-Category, Order Date
The x-axis is hierarchically structured. Each year contains multiple product sub-categories, while the sub-categories are organized within their broader product categories.
For example, products such as Bookcases, Chairs, Furnishings, and Tables appear together within their corresponding category structure.
### Analytical purpose
This visualization establishes a baseline for comparing:
1. Sales magnitude across products
2. Year-over-year changes
3. Regional differences
4. Sales versus profitability
The default view focuses on the <b>South region</b>, but users can change the regional selection to investigate other regions such as Central, East, and West.
This allows the same visualization to answer questions such as:
* Which sub-categories have the highest sales?
* Does sales growth appear consistent across years?
* Which high-sales products have relatively weak profit?
* Does product performance vary substantially by region?
### Visual encoding
The use of color is particularly important here.
A tall bar indicates <b>high sales</b>, while the bar’s color indicates the corresponding <b>profitability</b>.
This prevents the analysis from equating sales performance with business success. A product with high sales may still exhibit weak or negative profit.

<img width="2030" height="1926" alt="Regional_Sales_and_Profits_Tab1" src="https://github.com/user-attachments/assets/373014a0-875d-454e-a46e-8fbaad5a9521" />

⸻
 
## Tab 2 — Machine Sales by Year

### Purpose
The second story point narrows the analysis from the complete product portfolio to the <b>Machines</b> sub-category.
This is the first major analytical drill-down.
### Visualization
The dashboard displays a bar chart of Machine sales across:<b>2019 → 2020 → 2021 → 2022</b>
* <b>X-axis:</b> Year / Machines
* <b>Y-axis:</b> Sales
* <b>Color:</b> Profit
The Region filter remains available, allowing the user to investigate machine performance within different regions.
### Analytical purpose
This visualization isolates Machines because the later stages of the story investigate machine profitability in greater geographic detail.
The view helps identify:
* Changes in machine sales over time
* Years with particularly high or low sales
* Whether sales performance corresponds to profitability
* Whether regional selection changes the observed pattern
This creates a logical transition from the general product portfolio in Tab 1 toward the more focused machine-profit investigation in Tab 9.

<img width="2030" height="1926" alt="Regional_Sales_and_Profits_Tab2" src="https://github.com/user-attachments/assets/9db21309-b7ce-40de-a424-7d97400177f6" />

⸻


## Tab 3 — Underperforming Items in the South

### Purpose
After establishing the overall product and machine performance, the analysis shifts from <b>what is happening to where underperformance is occurring</b>.
This story point focuses specifically on the <b>South region</b>.
### Visualization 1 — Geographic Profitability Map
The upper visualization is a geographic map of the states within the South region.
The map displays:
* State-level profit
* Profit Ratio
* Geographic distribution of performance
The year can be changed, allowing the user to examine the geographic pattern for different years.
The current screenshot shows the <b>2020</b> view.
The geographic encoding makes it possible to identify states with weaker profitability without requiring the user to inspect each state individually.
### Visualization 2 — Sales by Product Sub-Category
The lower visualization displays sales across product sub-categories for the selected year.
* <b>Bar height:</b> Sales
* <b>Bar color:</b> Profit
<br>
The two views therefore provide complementary information:
<b>Map → Where is the performance problem?</b>
<b>Bar chart → Which products contribute to the observed performance?</b>
### Analytical purpose
The combination of geographic and categorical views supports a two-dimensional diagnostic process:
<b>Geographic identification → Product-level investigation</b>
Instead of treating the South region as a single aggregate, the visualization allows the user to identify individual states that may warrant deeper investigation.

<img width="2030" height="1926" alt="Regional_Sales_and_Profits_Tab3" src="https://github.com/user-attachments/assets/7a757538-28a0-466f-83c0-50980a91d0ef" />

⸻


## Tabs 4–8 — North Carolina Drill-Down
The next five story points focus specifically on <b>North Carolina</b>.
These tabs represent a temporal drill-down from the broader South-region analysis into one state.
 
⸻
 
## Tab 4 — Profit in North Carolina, 2019–2022
Tab 4 provides the overall North Carolina view across the complete 2019–2022 period.
### Upper visualization
The geographic map places North Carolina within the South region and highlights its profitability relative to surrounding states.
In the displayed view, North Carolina shows:
* <b>Profit: approximately -$7,491</b>
* <b>Profit Ratio: approximately -13%</b>
The map therefore establishes North Carolina as an area requiring further investigation.
### Lower visualization
The lower bar chart decomposes North Carolina’s performance by:<b>Year → Product Sub-Category</b>
The chart covers:
* 2019
* 2020
* 2021
* 2022
with:
* <b>Bar height = Sales</b>
* <b>Color = Profit</b>
This makes it possible to compare both the scale of sales and the profitability of different product sub-categories over time.
### Analytical question
The key question becomes:
<b>Is North Carolina’s weak profitability concentrated in a particular year or product sub-category?</b>


<img width="2030" height="1926" alt="Regional_Sales_and_Profits_Tab4" src="https://github.com/user-attachments/assets/ae0c0f9c-35f8-44fe-bd8e-dec350d87fca" />

⸻


## Tab 5 — Profit in North Carolina, 2019
Tab 5 isolates North Carolina’s performance in <b>2019</b>.
The visualization retains the same geographic and product-level structure as Tab 4 but restricts the analysis to one year.
This allows individual product-level patterns to be examined without the additional visual complexity introduced by multiple years.


<img width="2030" height="1926" alt="Regional_Sales_and_Profits_Tab5" src="https://github.com/user-attachments/assets/553dcc21-18e0-4c47-b4c1-cb935ec23909" />

⸻


## Tab 6 — Profit in North Carolina, 2020
Tab 6 applies the same analytical structure to <b>2020</b>.
The year-specific view allows the viewer to compare the product mix and profitability pattern against the previous year.


<img width="2030" height="1926" alt="Regional_Sales_and_Profits_Tab6" src="https://github.com/user-attachments/assets/05c13904-bedf-40e8-87ac-c2fba501951a" />

⸻
 
## Tab 7 — Profit in North Carolina, 2021
Tab 7 focuses on <b>2021</b>.
The year-specific visualization allows the viewer to determine whether profitability problems observed in earlier years persist, disappear, or shift toward different product sub-categories.


<img width="2030" height="1926" alt="Regional_Sales_and_Profits_Tab7" src="https://github.com/user-attachments/assets/faea30ad-21f7-404b-b46b-f89f11b423b0" />

⸻
 
## Tab 8 — Profit in North Carolina, 2022
Tab 8 focuses on <b>2022</b>.
This is particularly important because the final story point also investigates machine profitability in North Carolina during 2022.
Consequently, Tab 8 acts as the bridge between the broader state-level analysis and the final city-level investigation.


<img width="2030" height="1926" alt="Regional_Sales_and_Profits_Tab8" src="https://github.com/user-attachments/assets/66195604-98bf-4df6-a28f-80f5239d0158" />

⸻


## Tab 9 — Where Are We Losing Machine Profits in North Carolina in 2022?
### Purpose
The final story point represents the deepest level of the analytical drill-down.
After identifying North Carolina as an area of concern and examining its performance across years, the analysis focuses specifically on:
<b>Machines → North Carolina → 2022 → City</b>
### Visualization
The primary visualization is a hierarchical horizontal bar chart.
The hierarchy is:
<b>Country/Region → State/Province → City → Sub-Category</b>
The x-axis represents: <b>Profit</b>.
Negative values extend to the left, making profit losses immediately visible.
### Analytical question
The visualization addresses a more specific diagnostic question:
<b>Where are machine-related profits being lost within North Carolina in 2022?</b>
The dashboard reveals substantial negative machine profit in <b>Burlington, North Carolina.</b>
The highlighted observation indicates that: <b>Machines in Burlington lost nearly $4,000 in profit in 2022.</b>
This is an important transition in the analytical story because the investigation has moved from an aggregate regional metric to a highly specific combination of: <b>State + City + Product Sub-Category + Year</b>
The result demonstrates how visualization can be used not only to identify an underperforming region, but also to trace the problem to a more granular geographic and product level.


<img width="2030" height="1926" alt="Regional_Sales_and_Profits_Tab9" src="https://github.com/user-attachments/assets/d43f3375-1dfc-46b1-bc2d-c0903cf02521" />

⸻
 

## Key Analytical Insights
The dashboard is designed primarily as an <b>exploratory analysis</b>, so the main value is not a single predetermined conclusion but the ability to discover patterns through progressive filtering and drill-down.
Several observations emerge from the current dashboard:
<b>1. Sales and profitability do not necessarily move together</b>
The use of Sales as bar height and Profit as color makes it possible to identify products that generate substantial sales but comparatively weak or negative profit.
This distinction is important because optimizing for sales alone could overlook economically inefficient products.
<b>2. Machine performance warrants additional investigation</b>
The dedicated Machine view indicates that Machines represent an important sub-category for further analysis.
This motivates the subsequent geographic investigation.
<b>3. Geographic aggregation can hide local problems</b>
The South-region map provides a high-level view of state performance.
However, the later North Carolina analysis demonstrates why state-level aggregates may not be sufficient for diagnosis.
A state can contain cities and products with very different profitability patterns.
<b>4. North Carolina emerges as an important area for investigation</b>
The North Carolina story points show a substantial negative profitability figure over the 2019–2022 period and allow the user to examine how this performance develops across individual years and product sub-categories.
<b>5. The final drill-down identifies Burlington as a major source of machine profit loss</b>
The final visualization highlights a machine-related profit loss of nearly <b>$4,000 in Burlington during 2022</b>.
This provides a concrete example of how a broad profitability problem can be progressively decomposed into a specific geographic and product-level issue.
 
⸻


## Analytical Workflow
The project can be summarized as the following analytical workflow:

Overall Sales & Profit Performance
              │
              ▼
      Product Sub-Categories
              │
              ▼
        Focus on Machines
              │
              ▼
     South Region Analysis
              │
              ▼
     Identify Weak States
              │
              ▼
      North Carolina
              │
              ▼
       Year-by-Year Analysis
              │
              ▼
          2022 Focus
              │
              ▼
        City-Level Analysis
              │
              ▼
    Machine Profit Loss in
          Burlington

This progression is intentional. Each stage reduces the analytical scope while increasing the level of detail.
 
⸻


## Visualization Techniques Used
The project demonstrates several core data visualization techniques in Tableau.
### Bar Charts
Used for:
* Sales comparison
* Year-over-year comparison
* Product sub-category comparison
* Profit-loss analysis
Bar charts provide a straightforward way to compare quantitative values across categorical dimensions.
### Geographic Maps
Used to:
* Compare profitability across states
* Identify geographically concentrated underperformance
* Highlight North Carolina within the South region
### Color Encoding
Profit is encoded using a continuous diverging color scale.
This provides an additional quantitative dimension without requiring a second axis.
### Hierarchical Dimensions
Several views use hierarchical structures such as:
Year
 └── Category
      └── Sub-Category
and:
Region
 └── State
      └── City
           └── Sub-Category
This supports progressively more granular analysis.
### Interactive Filtering
Users can change the analytical scope by selecting:
* Region
* Year
* Sub-Category
This allows the dashboard to function as an exploratory tool rather than a fixed presentation.
### Tooltips
Hover interactions provide additional information without overcrowding the visual canvas.
This follows the principle that supporting information can be revealed on demand rather than displayed permanently. 
 
⸻


## Design Rationale
The visualization design emphasizes <b>analytical clarity over decorative complexity.</b>
Rather than placing many unrelated charts into one dashboard, the workbook distributes the analysis across multiple story points. This allows each view to answer a narrower question while preserving the overall analytical narrative.
The design follows three principles:
<b>1. Progressive Disclosure</b>
The dashboard does not expose every level of detail immediately.
Instead, the viewer moves from:<b>Region → State → City → Product</b>
This reduces cognitive overload while maintaining analytical depth.
<b>2. Multiple Encodings for Complementary Measures</b>
Sales and Profit are represented through different visual channels:
* Position/length → Sales
* Color → Profit
This enables simultaneous comparison of sales volume and financial performance.
<b>3. Context Before Detail</b>
The story first establishes the overall regional and product context before focusing on North Carolina and individual cities.
This makes the later findings easier to interpret because the viewer understands the broader geographic context first.
These choices are consistent with Tableau’s recommendation to give a dashboard a clear purpose, limit unnecessary visual complexity, and use interactive elements to support exploration. (Tableau Help⁠)
 
⸻


## Technical Skills Demonstrated
This project demonstrates practical experience with:
* <b>Tableau</b>
* Data visualization
* Dashboard development
* Data storytelling
* Geographic visualization
* Hierarchical data analysis
* Time-series comparison
* Interactive filtering
* Tooltip design
* Categorical and quantitative encoding
* Profitability analysis
* Exploratory data analysis
* Business-oriented analytical reasoning
More importantly, the project demonstrates the ability to translate a relatively multidimensional business dataset into a structured analytical interface.
 
⸻


## Research-Oriented Perspective
Although this project is business-oriented, its structure also demonstrates several skills relevant to research-oriented data analysis.
The visualization process follows a general analytical pattern:
<b>1. Define an analytical question</b>
<b>2. Identify relevant dimensions and measures</b>
<b>3. Explore aggregate patterns</b>
<b>4. Identify potential outliers or underperforming groups</b>
<b>5. Condition the analysis on geographic and temporal dimensions</b>
<b>6. Drill down to more granular observations</b>
<b>7. Generate hypotheses for further investigation</b>
For example, the discovery of substantial machine losses in Burlington does not by itself establish why the losses occurred. Instead, it identifies a potentially important observation that could motivate further analysis.
Possible follow-up questions include:
* Which individual machine products contributed to the loss?
* Were the losses caused by low prices, high costs, discounts, or other factors?
* Was the pattern persistent across multiple orders?
* Did Burlington behave differently from comparable cities?
* Are the losses associated with a particular customer segment?
* Are similar machine-profit problems present in other regions?
This distinction between <b>descriptive discovery</b> and <b>causal explanation</b> is important. The current project is primarily exploratory and descriptive; the identified patterns could serve as starting points for subsequent statistical or causal analysis.
 
⸻
 

## Limitations
Several limitations should be considered when interpreting the dashboard.
### Descriptive rather than causal
The visualization identifies patterns and potential problem areas but does not establish causal relationships.
For example, identifying negative machine profit in Burlington does not explain the underlying cause of that loss.
### Aggregation effects
Some visualizations aggregate data at the region, state, year, or sub-category level. Aggregation can conceal variation among individual transactions, customers, or products.
### Profit Ratio definition
The dashboard uses a Profit Ratio measure in the geographic views. The current README intentionally does not specify its mathematical formula because the exact calculated-field definition is not documented in the project materials.
### Scope of variables
The current analysis focuses primarily on Sales, Profit, geographic dimensions, product categories, and year. Additional variables could provide further explanatory power in a subsequent analysis.
 
⸻


## Potential Extensions
The project could be extended in several directions.
### Statistical Analysis
The exploratory findings could be followed by statistical analysis to determine whether observed differences across regions, years, or product categories are statistically meaningful.
### Profit Driver Analysis
A follow-up analysis could investigate the factors associated with negative profit, such as:
* Product
* Discount
* Customer segment
* Order characteristics
* Geographic location
* Time
### City-Level Comparison
Burlington could be compared with other cities in North Carolina or with similar cities in other regions to determine whether the observed machine losses are unusually large.
### Predictive Modeling
Machine-learning models could potentially be used to identify transactions or product combinations associated with elevated profit-loss risk.
### Causal Analysis
If appropriate data were available, causal methods could be used to investigate whether specific business decisions or interventions contributed to changes in profitability.
 
⸻
 

## Project Takeaways
This project demonstrates how an interactive visualization can transform a multidimensional sales dataset into a structured analytical narrative.
The main contribution of the dashboard is not simply the production of charts, but the organization of those charts into a coherent sequence:
<b>Explore the overall performance → identify an area of concern → narrow the geographic scope → examine temporal variation → identify the product dimension → locate specific sources of loss.</b>
The final result is an interactive Tableau story that connects </b>business-level metrics with geographic and product-level detail</b>, while allowing users to investigate the data independently through filters and interactions.
From a data analytics perspective, the project demonstrates the importance of moving beyond aggregate metrics. A regional profitability problem becomes more actionable when it can be traced to a particular state, year, city, and product sub-category.
 
⸻


## Tools
|Tool|	Purpose|
|----|--------|
|Tableau|	Data exploration, visualization, dashboard development, and interactive storytelling|
|Tableau Public|	Publishing and sharing the interactive visualization|
|GitHub|	Project documentation and portfolio presentation|
 
⸻
 
## Tableau Public
Open the interactive Tableau Public visualization⁠
 
⸻


## Repository Structure
Regional-Sales-and-Profits-Project/
│
├── README.md
│
├── Tableau/
│   └── Regional Sales and Profits.twb
│
├── Screenshots/
│   ├── tab01-sales-profit-by-year.png
│   ├── tab02-machine-sales-by-year.png
│   ├── tab03-underperforming-items-south.png
│   ├── tab04-north-carolina-2019-2022.png
│   ├── tab05-north-carolina-2019.png
│   ├── tab06-north-carolina-2020.png
│   ├── tab07-north-carolina-2021.png
│   ├── tab08-north-carolina-2022.png
│   └── tab09-machine-profit-loss-north-carolina-2022.png
│
└── Data/
    └── Regional Sales and Profits Data.csv
 
⸻
 

## Author
#### Keman Xiang
This project is part of my data analytics and visualization portfolio, demonstrating practical experience in <b>Tableau, exploratory data analysis, business analytics, and interactive data storytelling.</b>
