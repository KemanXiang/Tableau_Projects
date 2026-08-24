# Visualization Project CO2 Emission per Capita for Each Country -- Link Multiple Datasets in Tableau

[x](https://public.tableau.com/app/profile/keman.xiang/viz/Week2_01_CO2_DATA/Sheet1)

## Activity overview
In this project, we will review a scenario, link different data sources in Tableau using JOINs, and create visualizations using multiple datasets.

## Objective
Make visualizations out of data from multiple sources. 

## The scenario
Imagine we are working as data analysts at a policy research institute. For our current project, we need to create a visualization that shows the CO2 emissions per capita for each country from 2000-2011. We need to provide a visual presentation that not only allows someone to visually compare CO2 emissions between countries from year to year, but also provides information about each county’s population, GDP, and energy use. 

We already have a dataset that includes emissions for each country between the years 1960 - 2011. But, the information that we need on energy use, total population, and GDP we had to collect from a government website. Each dataset is in a separate file. Moreover, some of the information is missing for some countries. 

Often we will work with datasets that are missing information. Whether or not we need to find this missing information will depend on the project. In this case, we will notice that the missing information is from the 1960s, 1970s, and 1980s. 

Luckily, our project is only concerned with the data from 2000-2011. We need an efficient way to utilize some data from one source, and some data from other sources. Taking just the information that we need from each source and creating a new data source takes a lot of time. 

Tableau allows us to link data from different sources, as well as import data from different formats. Tableau allows you to use a Web Data Connector, this tool allows us to import the data we need directly from another site. Our visualizations will update when the data sources for our visualization are updated.

## Load the data

1. Log in to Tableau Public and Create a Viz.
2.  Open the CO2 dataset.
3. From the Data Source tab - Connections, add another data source. Start with the energy dataset.
4. Repeat for the other datasets, gdptotal and totalpopulation.

Now, we should have all four datasets loaded into Tableau. The datasets will be on the left-hand side of our screen under Connections. 
![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ElL7gKUVQbqS-4ClFfG6LQ_30e09cb76f15476187ebc8aa77fa52e1_DAC6M2L4SR1-SS2.png?expiry=1787652949288&hmac=lMbqHqfwHZAXj1mjl6FjGlnvoXvPrpdZ1R-mersXmdU)

## Make connections with JOINs

Now, we’ll set up the connections between the different datasets by creating JOINs between them. 

INNER JOINs and OUTER JOINs are types of relationships that can be used to combine data based on common columns of information.

In Tableau, we’ll notice that the former JOINs window has now become a multi-purpose Relationships window. By double-clicking the data tables, we can edit the JOINs instead of the relationships. 

1. Click on CO2 under Connections. 
2. Under Sheets, we will notice all the different sheets in the CO2 dataset. Find CO2 Data Cleaned and double-click on it to load it.
3. Hover the cursor over the right side of the CO2 Data Cleaned box and click on the arrow.
4. Select Open to open the CO2 Data Cleaned dataset. This allows us to change the physical table, which will allow us to create JOINs. Otherwise, we will only be able to edit Relationships. Usually, we could use either option to accomplish the same goal. But for the purposes of this activity, we specifically want to use JOINs.

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UqyTapQ1QhGsk2qUNfIRtw_a7c3d0cc5b9b459d869288ecf0edc1f1_Screenshot-2021-06-06-4.58.30-PM.png?expiry=1787652949287&hmac=mMgd-cvMq-Uvw7wyMxjFADbcHiF0wAEDS90P4XS-ZoA)

5. Click on the energy dataset under Connections.
6. Drag the energy sheet across from the CO2 Data Cleaned box under Multiple Connections. A pop-up window for a Join will appear.
7. The popup window may automatically populate with Year from CO2 Data Cleaned and Year1 from Energy. If not, put Year on the left side of the chart and Year1 on the right side.
8. Click on Add new join clause under Year. A dropdown menu will appear.
9. Select Country Name on the left side and Country on the right side.
10. Click the X to close the dropdown menu.

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/lIBshvhNTneAbIb4TS53fw_83ad47273215482bbc58083435fe6df1_join-table.png?expiry=1787652949288&hmac=KsT90Gh59QwlBRv0Y8kMee6rmv8fg8dnzAqxCq_OXOE)

11. Click Update now to examine the dataset. We will notice that Year and Year1 have a number sign above them. Change the data type to date for each of these columns. 
12. In the column, Year click on the # (not the arrow next to it) and select Date from the available options. 

After completing the first field, we will notice a red exclamation mark between CO2 Data Cleaned and Energy. This indicates that the columns we have joined are no longer of the same data type. One is formatted as date, and the other numeric.

We will also notice that after changing Year (CO2 Data Cleaned) to a Date type, the data preview pane will no longer display properly.

13. To fix this, go to the column list in the lower left of the screen. 
14. Select the # icon next to the Year1 (Energy) column. Then, change the data type to Date.
Click Update Now in the preview pane to display the data properly. 

The red exclamation mark will disappear. We might notice that all the years have been put into a month/day/year form with the default month and day as January 1st. This will not create any problems when creating a visualization, as we will filter the data by year.

## Connect additional datasets

Before adding any additional joins, the data type for Year(Gdptotal) needs to change. 

A pop-up window will appear for the join. It might already be populated with Year1 under Datasource and Year(Gdptotal) under gdptotal.

1. Click on gdptotal under Connections.
2. Under Sheets, drag the gdptotal sheet into the white space underneath the energy box.  
3. Go to the column list in the lower left of the screen, scroll to find the column Year(Gdptotal). Click on # above it. A drop-down menu will appear.
4. Select Date from the drop-down menu.
If the data preview does not display properly, fix the date type in the lower left pane.
5. Click on the Venn diagram between energy and gdptotal. Click on Add new join clause under year. A drop-down menu will appear. 
6. Under CO2 Data Cleaned click on Country Name. 

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/K4_JxDVaTFKPycQ1WrxSYw_9c604f9425d64f8fa2f23fc2f73883f1_realdropdown.png?expiry=1787652949288&hmac=Bi77HG-JduTdWUI7FVsoJieqVkgBLIJsAK_M8d-wBUY)

7. Click on the empty field under gdptotal across from Country Name. A dropdown menu will appear.
8. Set the right side of the join statement to Country1.
9. Close the Join pop-up by clicking on its exit button.

Now we are going to join totalpopulation.

10. Click on totalpopulation under Connections.
11. Under Sheets, drag the totalpopulation sheet into the white space to the right of the energy and gdptotal boxes. 
A pop-up window will appear for the join. It should already be populated with Year under Datasource and Year(totalpopulation) under totalpopulation.
12. Go to the column list in the lower left of the screen, scroll to find the Year(totalpopulation) column. Click on # above it. A drop-down menu will appear.
13. Select Date from the drop-down menu.
If the data preview does not display properly, fix the date type in the lower left pane.
14. Click on the Venn diagram to the left of totalpopulation. Click on Add new join clause under Year. A drop-down menu will appear. 
15. Under CO2 Data Cleaned click Country Name. 
16. Click on the empty field under totalpopulation across from Country Name. A dropdown menu will appear.
17. Click Country (totalpopulation).
18. Close the Join pop-up by clicking on its exit button.
19. Click the Update button to view your data columns.

Congratulations! Now we have successfully joined four different sources of data.

As we study our dataset, we should notice that years in our dataset are between 2000-2011. While our dataset CO2 went from 1960-2011, and our other datasets went from 2000-2015, the intersection (the years they have in common) only includes 2000-2011. This is just the time span that we need. 

If the dataset had gone beyond those dates, we would have filtered out the unneeded years in our visualization.

Reviewing the dataset, we also noticed that some of our measurement values need to be changed. The data type for the column Energy use is listed as string data. We can tell this because of the Abc icon above the name. The column currentGDP is also formatted as type string.

20. Find the Abc icon above the Energy use column. Change it to Number (decimal).
21. Find the Abc icon above the currentGDP column. Change it to Number (whole).
If the data preview does not display properly, fix the date type in the lower left pane.

## Create a visualization

1. Click on the tab Sheet1.
2. Drag Country Name under CO2 Data Cleaned into the Detail square.

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9L2gBHrSTCK9oAR60jwitA_4467ebb8030f49838f935b6336c84c5b_send1.png?expiry=1787652949287&hmac=En-AcmYJK2kO_EnhVei1P_Gsfxrqrz1Xu8RB3DyX7hA)

3. Drag CO2 Per Capita to Color.
4. Click on Color, then Edit Colors.
5. Click on the Palette dropdown and change it from Automatic to Red-Green diverging.
6. Check the boxes for Stepped Color and Reversed. (Because green is generally viewed as positive for CO2 emissions, we want the colors to move towards red as emissions go up.)
7. Click the Show Advanced dropdown.
8. Check the Start and End boxes.

We also noticed that the legend on the right-hand side of the screen shows Sum(CO2 per capita). We need to change the start and end values in order to notice color contrasts showing red shades. 
The lowest CO2 Per Capita emission for any year is 0.0396 and the largest is 61.9898. 

9. Enter 0 into the Start field, and 62 into the End field. Click OK. Click the X button.
Note: These values are the highest and lowest emissions between 2000-2011.

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Dy9EYpbvTJ6vRGKW7xye1g_d2d01901c6d94693a60ce96acbbdadf1_rgdiv.png?expiry=1787652949289&hmac=aJUvnA32QkvsJQkILoM_m--o__YBnONPrd0ijtzk7DU)

11. Drag Year from under CO2 Data Cleaned into the Filters area.

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/BOdEa3alR5qnRGt2pfeanQ_388635cd400f478598eaa8c36d59269c_image.png?expiry=1787652949288&hmac=ZzBZtzltqTBDGqeohWCXEqSDABji8VZNi8WEDu3yjqQ)

12. Click on Years, Next, All, OK.
13. In the Filters box, right-click on YEAR(Year)
14. Select Show Filter. The filter will appear on the right side of the screen. 

![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/wFlWJpkZShiZViaZGeoYGA_a132a5f43de54262abc1b9e2b2e774e4_Screen-Shot-2021-04-07-at-8.04.10-PM.png?expiry=1787652949288&hmac=tyj-143r19PMk9MmtyFC-hH0OuMj_TZZmsIVHfAUh4U)

15. Click on the arrow to the right of YEAR(Year) on the far-right side of the screen.
16. Select Single Value (dropdown). Now the areas are colored only for the values of each year. Use the checkboxes in the list to choose which years we want to include in the visualization. We can select only the years between 2000-2011 to view the emissions relevant to the scenario.

Now we've linked our data and made a comprehensive data visualization in Tableau.
