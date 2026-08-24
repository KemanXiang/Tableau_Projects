
# Create Data Visualization of CO2 Emissions in Tableau

View my project Dashboard on [Tableau Public](https://public.tableau.com/views/Week1_02_GlobalC02Emissions/Sheet1?:language=zh-CN&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
<div class='tableauPlaceholder' id='viz1787565206712' style='position: relative'><noscript><a href='#'><img alt='Global C02 Emissions ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;We&#47;Week1_02_GlobalC02Emissions&#47;Sheet1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Week1_02_GlobalC02Emissions&#47;Sheet1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;We&#47;Week1_02_GlobalC02Emissions&#47;Sheet1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='zh-CN' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1787565206712');                    var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>

## Activity overview
Tableau is a powerful, free-to-access software tool used for visualizing data. In this project, we will utilize the Tableau basics for creating and editing charts.

## Objective
Create and customize visualizations in Tableau. 

## Create a chart 

1. Log in to Tableau Public and create a Viz.
2. This may bring us to the Connect to Data window. Go to the Files tab and open the CO2 dataset. 
3. Once we have uploaded the data, we will notice the following display. Locate the sheets contained in the data file on the left side of the screen.

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/JvtiAAUYRzW7YgAFGMc15g_f4dc1e733f5e413296bbcbe0d4ee3780_Tableau1.png?expiry=1787650725085&hmac=C0mFOVFX9Kug33wEqBXNxGd7tfj-AODZWmWJzTeHQBg)

A left-side menu containing a list of sheetsSheets:
- About
- CO2 (kt) for Split
- CO2 (kt) Pivoted
- CO2 (kt) RAW DATA
- CO2 (kt) Cleaned
- CO2 (kt) Per Capita (Pivoted)
- CO2 (kt) CO2 Per Capita RAW DATA
- Metadata - Countries
4. Double-click on the sheet CO2 Data Cleaned to load that sheet's data into the main part of the screen. We can also drag and drop the sheet into the area where it says Drag tables here.
Once this is done, the main display will appear like this:
![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/QlMviRQiRbeTL4kUIoW3AA_f147895d16ef4b86bf40a5db62e6d75e_Tableau2.png?expiry=1787650725085&hmac=IAAG0IDbeF0zQ_y54bY3e5fAC8uiPckf4NJjso0_i80)

The data in the table are listed in the bottom portion of the display above. By default, Tableau will only show the first 1000 rows in the table, but we can increase the number of rows in the settings above the data view.

Each row corresponds to a single data point, and each column represents a different feature.

Tableau interprets the type of data in each column. The following icons, which are above in the column name, refer to how Tableau interprets the data type in the column:

- #: Numeric data
- Abc: String data
- Globe: Geographic data
- Calendar: Date data
- Calendar with a clock: Date and time data

In the image above, we can see that Tableau has interpreted the first two columns as geographic data, the third column as string data, and the last three columns as numeric data.

## Create a visualization of CO2 emissions

Now that we have all of the data loaded into Tableau, we can use it to make visualizations. Create a visualization in which the <b>CO2 emissions</b> are displayed <b>per country</b>.

First, click on the Sheet1 tab
![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/HzB_GAw8SpmwfxgMPLqZ_A_45df0abe1a0841d4a0ff0dda6c908f54_image10.png?expiry=1787650725085&hmac=0rKW0x6-WAG2QoX5tibtWuovDT6j0QL2S7JB-xogI10)

### Use dimensions and measures
On the far left of the screen is a banner with column names above a grey line. In Tableau, these are called the <b>dimensions</b> of the data. Below this line are the different measures that we can track for these dimensions. 

Now, let's create a chart that displays the CO2 emissions per country. The main display will show a map of the countries on the planet with dots indicating which countries are represented in the data.
![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/99hzCey_SviYcwnsv7r4BQ_72545e3514124a7db933dd0563384892_image7.png?expiry=1787650725085&hmac=ax66iPs1xoEKyiY635Di5dsHat9b2EVBmtQVfXemrnk)

The dots are all the same size because—with no measure selected—Tableau defaults to scale each country equally. If we want to scale by CO2 emissions, we need to include a specific measure.

As we choose the measure CO2 (kt). This will change the size of the dots to be proportional to the amount of CO2 emitted like below.
![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/sFaJs-zZSdmWibPs2SnZFQ_b85e5efecfa94eeaac90152f93501a85_DAC6M2L2SR1_ss6.png?expiry=1787650725085&hmac=Ux59NNKzThF28W9YfsiF-PRMLUKpBmlpfEkqFkP3lGI)

Tableau has a wide selection of options for depicting the measure for a given dimension. Most of these options are contained in the middle column between the main display and the column with dimensions and measures.
![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Wmt0VF_NQcSrdFRfzUHEAA_7492831a777548b08815359426f4251f_DAC6M2L2SR1_ss6.1.png?expiry=1787650725085&hmac=ytwqNcFCoUgbH4IxfbpBhzPCJYXnanfpPCHle2LPWrY)

## Customize the Chart

If we drag and drop a measure on one of the option classes, such as Color, Size, and Label, we can change that aspect of the measure’s visualization on the chart. 

Let's change the color of the CO2 measure, drag the measure CO2 (kt) to the box with the Color label. Then, click on this box to pull up a list of options for the colors we can use.

### Change dimensions and measures

Suppose that instead of visualizing the CO2 per country, we want to chart the CO2 per capita per region.

To do this, double-click on the dimension Region and then do the same for the measure CO2 Per Capita. This will result in a new chart like below:
![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/u93ytTllTmid8rU5Ze5oxA_3de43f4b42ac4195bb78f8679b776e3a_image16.png?expiry=1787650725085&hmac=RJl8h1d89LI1im-N6nhFHcDwiz9-GYlNG3s1HakCqOA)

Now our visual is complete.
