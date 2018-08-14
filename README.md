
# Data Visualisation with Tableau

#### Our goal as Data Analysts is to arrange the insights of our data in such a way that everybody who sees them is able to clearly understand their implications, or their truths and how to act on them.

#### Tableau is the widely used data analytics and visualization tool that many consider indispensable for data-science-related work. Its drag-and-drop interface makes it easy to sort, compare, and analyze data from multiple sources, including Excel, SQL Server, and cloud-based data repositories.

#### In this tutorial, we will learn how to analyze and display data using Tableau and make better, more data-driven decisions. This tutorial will cover the following topics:

* #### [1. Introduction to Tableau](#introduction-to-tableau)
   * Overview
   * Installation

* #### [2. Getting Started](#getting-started)
   * Tableau Workspace
   * Connecting  to a Data Source 
   * Creating a view
   * Refining the view

* #### [3. Emphasize the Results](#emphasise-the-results)
   * Adding Filters to the view
   * Adding Colors to the view
   * Key Findings

* #### [4. Map View](#map-view)
   * Building a Map View
   * Getting into details
   *  Identifying the Key points

* #### [5. Dashboard](#dashboard)
   * Creating a dashboard
   * Adding Interactiveness 

* #### [6. Story](#story)
   * Building a Story
   * Making a Conclusion

* #### [7. Saving the Work](#saving)





# <a name="introduction-to-tableau"></a>1.Introduction to Tableau

## Overview

[Tableau Software](https://www.tableau.com/)  is an American computer software company headquartered in Seattle, WA, USA. It generates interactive data visualization products which focused on BI. The company was established at Stanford University’s Department of Computer Science between 1997 and 2002.

The main products offered by  tableau are:

![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Introduction%20to%20tableau/Tableau%20Product%20suite.png)

### **Tableau Desktop, Tableau Public, and Tableau Online**, all offer Data Visual Creation and choice depends upon the type of work

![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Introduction%20to%20tableau/Tableau%20Products.png)

> ### In this tutorial, we will be working with Tableau Desktop.


## Installation

Depending upon the choice of product, download the software on to the computer. In this tutorial, we will be working with Tableau Desktop version. The installation is a very straightforward process in which you need to accept the license agreement. You can verify the installation by clicking the Tableau Icon. If the following screen appears, you are good to go.

![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Introduction%20to%20tableau/installation.png)




# <a name="getting-started"></a>2.Getting Started


In this section, we will learn some basic operations in Tableau to get acquainted with its interface.

## Tableau Workspace

The Tableau workspace consists of menus, a toolbar, the Data pane, cards and shelves, and one or more sheets. Sheets can be worksheets, dashboards, or stories. The image below highlights the major components of the workspace. However, more familiarity will be achieved once we work with actual data.

![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/getting%20started/Tableau%20Workspace.png)


## Connecting to a Data Source

Before we can build a view and analyze our data, Tableau must be first connected to the intended data. Tableau supports connection to a wide variety of data, stored in a variety of places. For example, your data might be stored on your computer in a spreadsheet or a text file, or in a big data, relational, or cube (multidimensional) database on a server in your enterprise. Or, you might connect to public domain data available on the web such as U.S. Census Bureau information, or to a cloud database source, such as Google Analytics, Amazon Redshift, or Salesforce.

When you launch Tableau Desktop, the data connectors that are available to you are listed on the `Connect` pane, which is the left pane on the `Start page`. File types are listed first, then common server types, or servers that you've recently connected to. Click `More` to see the complete list of data connectors you can use. Under `Open`, you can open workbooks that you have already created. Under `Sample Workbooks`, view sample dashboards and worksheets that come with Tableau Desktop. Under `Discover`, find additional resources like video tutorials, forums, or the “Viz of the week” to get ideas about what you can build.


### `Hands On `     

	  
![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/getting%20started/connecting_to_dataource.gif)


For supported files and databases, Tableau provides built-in connectors that are built for and optimized for those types of data. If your file or database type is listed under Connect, use this named connector to connect to your data. If your file or database type is not listed, you might have the option of creating your own connection using Other Databases (ODBC) or Web Data Connector. Tableau provides limited support for connections that you create using either of these options


#### Connecting to the [Sample-Superstore data set](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/Data%20Visualisation%20with%20Tableau/Sample-Superstore%20.xls)

For convenience, let’s use the sample data set that comes with Tableau installation named sample superstore.xls.However, in this tutorial, we will download it from here and load it as an excel sheet. 
The data is that of a United States’ Superstore. It contains information about products, sales, profits, and so on that you can use to identify key areas for improvement within this fictitious company.

###  `Steps`

> 1. Import the Data into tableau workspace from the computer.
> 
> 2. Under the Sheets Tab, three sheets will become visible namely Orders, People, and Returns. However, we will focus only on Orders data. Double click on Orders Sheet and it opens up just like a spreadsheet.
> 3. We observe the first three rows of data looks a bit different and is not in the desired format. Here we make use of Data Interpreter, also present under Sheets Tab. By clicking on it we get a nicely formatted sheet. If you wish to view the exact changes that it made, click on Review the results, and choose the Orders tab in the opened Excel sheet. it will show, it simply removed the erroneous data.


### `Hands On `  

![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/getting%20started/connectingToData2.gif)


## Creating a View

We will start by creating a simple chart. In this section, we will get to know our data and will start to ask questions about the data to gain insights There are some important terms that we will encounter in this section.

| ` Dimension`      | `Measures`          | `Aggregation`|
| -------------     |:-------------:      |  -----------:|
| Dimensions are qualitative data, such as a name or date. By default, Tableau automatically classifies data that contains qualitative or categorical information as a dimension, for example, any field with text or date values. These fields generally appear as column headers for rows of data, such as Customer Name or Order Date, and also define the level of granularity that shows in the view.     | Measures are quantitative numerical data. By default, Tableau treats any field containing this kind of data as a measure, for example, sales transactions or profit. Data that is classified as a measure can be aggregated based on a given dimension, for example, total sales (Measure) by region (Dimension). | Row-level data rolled up to a higher category, such as the sum of sales or total profit. Tableau does this automatically so you can break data down to the level of detail that you want to work with. |

###  `Steps`

> 1. Go to the worksheet. Click on the tab `Sheet 1` at the bottom left of the tableau workspace.
> 
>   ![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/getting%20started/creating%20a%20view.png)
> 
> 2. Once, you are in the worksheet, from Dimensions in the Data pane, drag Order Date to the Columns shelf.
>
>   *When you drag Order Date to the columns shelf, Tableau creates a column for each year in your data set. Under each column is an Abc indicator. This indicates that you can drag text or numerical data here, like what you might see in an Excel spreadsheet. If you were to drag Sales to this area, Tableau creates a cross-tab (like a spreadsheet) and displays the sales totals for each year.*
> 
> 3. From Measures, drag Sales to the Rows shelf.
>
>   *Tableau generates a chart with sales rolled up as a sum (aggregated). Total aggregated sales for each year by order date is displayed.Tableau always generates a line chart for a view that includes time (in this case Order Date)*




### `Hands On `  

![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/getting%20started/creating%20a%20view.gif)

#### *This line chart shows that sales look pretty good and seem to be increasing over time. This is good information, but it doesn't really tell you much about which products have the strongest sales and if there are some products that might be performing better than others. Let us see what else you can find out.*



## Refining the View


Let us delve deeper and try to find out more insights regarding which products drive more sales. Let's start by adding the product categories to look at sales totals in a different way.

###  `Steps`


> 1. From Dimensions, drag `Category` to the Columns shelf and place it to the right of `YEAR(Order Date)`.The view updates to a bar chart.By adding a second discrete dimension to the view, data changes into discrete chunks instead of continuous. This creates a bar chart and shows the overall `Sales` for each `Product` category by year.
>
>    > `Learn More` 
>
>    > 1. To view information about each data point (that is, mark) in the view, hover over one of the bars to reveal a tooltip. The tooltip displays total sales for that category. Here is the tooltip for the Office Supplies category for 2017: 
>    >
>    >   ![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/getting%20started/Refining%20the%20view1.png)  
>    > 2. To add data point information as labels to your view, click `Show Mark Labels` on the toolbar. 
>    >
>    >   ![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/getting%20started/Refining%20the%20view2.png)
>    >
>    > 3. To display the bar chart horizontally instead of vertically, click Swap on the toolbar.
>    >
>    >   ![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/getting%20started/Refining%20the%20view3.png)

> 2. The view above nicely shows `sales` by `category` i.e furniture, office supplies, and technology. We can also infer that furniture sales are growing faster than sales of office supplies except for 2016. Hence it will be wise to focus sales efforts on furniture instead of office supplies. But furniture is a very broad category and consists of many different items. How can we identify which furniture item is contributing towards maximum sales?
> 
> #### **To help answer that question, we decide to look at products by `sub-category` to see which items are the big sellers. For example, for the Furniture category, you want to see details about   bookcases, chairs, furnishings, and tables. Double-click or drag the Sub-Category dimension to the Columns shelf.**
 
> #### **The sub-category is another discrete field. It creates another header at the bottom of the view and shows a bar for each `sub-category` (68 marks) broken down by category and year. However, it is a lot of data to visually make sense of. In the next section, we will learn about filters, color and other ways to make the view more comprehensible.**

### `Hands On `  

![Alt text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/getting%20started/Refining%20the%20viewgif.gif)


# <a name="emphasise-the-results"></a>3.Emphasise the Results

In this section, we will try to focus on specific results. Filters and colors are ways to add more focus to the details that interest us. 

## Adding filters to the view

Filters can be used to include or exclude values in the view. Here we try to add two simple filters to the worksheet to make it easier to look at product sales by sub-category for a specific year.

###  `Steps`

> In the Data pane, under Dimensions, right-click Order Date and select Show Filter.Repeat for Sub->category field also.  
> ![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Emphasize%20the%20Results%20/Adding%20filter.png)
> 
> #### **Filters are card types and can be moved around on the canvas by clicking on the filter and dragging it to another location in the view**
> 

## Adding colors to the view

Colours can be helpful in the visual identification of a pattern.

###  `Steps`
> In the Data pane, under Measures, drag Profit to Color on the Marks card.
> 
> ![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Emphasize%20the%20Results%20/adding%20color%5C.png)
> 
> #### **It can be clearly seen that Bookcases, Tables and even machine contribute to negative profit i.e loss. A powerful insight.**
> 

### `Hands On `  
![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Emphasize%20the%20Results%20/adding%20filter%20and%20color.gif)


## Key Findings
Let's take a closer look at the filters to find out more about the unprofitable products.

###  `Steps`

> 1.  In the view, in the `Sub-Category` filter card, clear all of the check boxes except `Bookcases, Machines,` and `Tables`. This throws an interesting fact. While in some years, Bookcases and Machines were actually profitable. However, in 2016, Machines became unprofitable.
> 2. Select `All` in the `Sub-Category` filter card to show all sub-categories again.
> 3. From Dimensions, drag `Region` to the `Rows` shelf and place it to the left of Sum(Sales). We notice that machines in the South are reporting a higher negative profit overall than in your other regions. 
> 4. Let us now give a name to the sheet. At the bottom-left of the workspace, double-click `Sheet 1` and type `Sales by Product and Region`.
> 5. In order to preserve the view, Tableau allows us to duplicate our worksheet so that we can continue in another sheet from where we left off.
> 6. In your workbook, right-click the `Sales by Product and Region` sheet and select `Duplicate` and rename the duplicated sheet to `Sales-South`.
> 7. In the new worksheet, from Dimensions, drag `Region` to the `Filters` shelf to add it as a filter in the view.
> 8. In the Filter Region dialogue box, clear all check boxes except South and then click `OK`. Now we can clearly focus on sales and profit in the `South`. We find that machine sales had a negative profit in 2014 and again in 2016. We will investigate this in the next section
> 9. Lastly, do not forget to save the results by selecting  `File > Save As`. Give your workbook a name, like `Regional Sales and Profits`.


### `Hands On ` 

![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Emphasize%20the%20Results%20/key%20findings.gif)


# <a name="map-view"></a>4.Map View 

## Creating a Map View

#### **Map views are very helpful when we are looking at geographic data (the Region field). In the current example, Tableau automatically recognizes that the Country, State, City, and Postal Code fields contain geographical information.**

### `Steps`

> 1. Create a new worksheet.
> 2. Add `State` and `Country` under Data pane to  `Detail` on the Marks card. We obtain the map view.
> 3. Drag `Region` to the `Filters` shelf, and then filter down to the `South` only. The map view zooms in to the South region, and there is a mark for each state.
> 4. Drag the `Sales` measure to `Color` on the Marks card. We obtain a filled map with the colors pointing to the sales in each state.
> 5. We can change the color scheme by clicking `Color` on the Marks card and selecting `Edit Colors`. We can experiment with the available palettes.
> 6. We observe that Florida is performing the best. Hovering over its mark reveals a total of 89,474 USD in sales, as compared to South Carolina, for example, which has only 8,482 USD in sales. Let us gauge the performance by `Profit` now since Profit is a better indicator than sales alone.
> 7. Drag `Profit` to `Color` on the Marks card. We now see that Tennessee, North Carolina, and Florida have negative profit, even though it appeared they were doing good in Sales. Rename the sheet as Profit Map


### `Hands On`

![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Map%20View/creating%20a%20map%20view.gif)


## Getting into the details


#### **Maps are great for visualizing the data broadly. In the last step, we discovered that we discovered that Tennessee, North Carolina, and Florida have a negative profit. In this section let us draw a Bar chart to explore the reason for the negative profit.**

### `Steps`

> 1. Duplicate the Profit Map worksheet and name it Negative Profit Bar Chart.
> 2. In the Negative Profit Bar Chart worksheet, click Show Me and then select horizontal bars. Show Me highlights different chart types based on the data you've added to your view.
> 3. Multi-select the bars on the left by clicking and dragging your cursor across the bars between Tennessee, North Carolina, and Florida. On the tooltip that appears, select Keep Only to focus on those three states.
> 
>    > **`Learn More`**  
>    >
>    > **Creating Hierarchies**   
>    > Hierarchies come in handy when we want to group similar fields so that we can quickly drill down between levels in the viz.
>     >
>     > 1. In the Data pane, drag a field and drop it directly on top of another field or right-click the field and select 
>     > 2. Drag any additional fields into the hierarchy. You can also re-order fields in the hierarchy by dragging them to a new position.
>     > In the current viz. we will create the following hierarchies: Location, Order and Product.  
>     > ![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Map%20View/Hierarchy.gif)
>     >
> 
> 4. On the Rows Shelf, click the plus icon on the `State `Field to drill-down to the `City` level of detail
> 5. That's a lot of data. We can use `N-Filter` to filter to reveal the poorest performers. From the Data pane, drag `City` to the Filters shelf. Click By field and then Click the `Top` drop-down and select `Bottom` to reveal the poorest performers. Type 5 in the text box to show the bottom 5 performers in the data set.
>     
> __We now see that Jacksonville and Miami, Florida; Burlington, North Carolina; and Knoxville and  Memphis, Tennessee are the poorest performing cities by profit.
There is one other mark in the view—Jacksonville, North Carolina—that doesn't belong, since it has profitable sales. This means there is an issue in the filter we applied. We will take the help of Tableau Order of Operations.__  

>  6. On the Filters shelf, right-click the Inclusions (Country, State) (Country, State) set and select Add to Context. We find that now Concord, North Carolina appears in view while Miami, Florida disappears which makes sense.  
>  7. But Jacksonville, North Carolina is still in the view which is incorrect. On the Rows shelf, click the plus icon on City to drill down to the Postal Code level of detail. Right-click the postal code for Jacksonville, NC, 28540, and then select Exclude.  
>  8. Drag Postal Code of the Rows shelf. This is the final view.  
>  ![](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Map%20View/getting%20into%20details.png)


     
### `Hands On`

![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Map%20View/getting%20into%20details.gif)
     
     
     
## Key Findings

#### **Let us now focus only on the loss-making entities i.e the Products and also let us identify the locations where such products are sold.**

### `Steps`

> 1. Drag Sub-Category to the Rows shelf.
> 2. Drag Profit to Color on the Marks card. This enables us to quickly spot products with negative profit.
> 3. In the Data pane, right-click Order Date and select Show Filter.It seems that Machines, tables, and binders don’t seem to be doing well. So should we stop selling those items in Jacksonville, Concord, Burlington, Knoxville, and Memphis? Let's verify.
> 4. Go back to the Profit Map sheet tab.
> 5. On the Data pane, right-click Sub-Category and select Show Filter.
> 6. From Measures, drag Profit to Label on the Marks card.
> 7. On the Data pane, right-click Order Date and select Show Filter to provide some context for the view.  Clear Binders, Machines, and Tables from the list on the Sub-Category filter card in the view.


### `Hands On`
    
![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Map%20View/key%20findings.gif)

# <a name="dashboard"></a>5. Dashboard


#### **A dashboard is a collection of several views, enabling one to compare a variety of data simultaneously.**

## Creating a Dashboard

### `Steps`
 
> 1. Click the `New dashboard` button.
> 2. Drag `Sales in the South` to the empty dashboard
> 3. Drag `Profit Map` to the dashboard, and drop it on top of the Sales in the South view. Both views can be seen at once. To be able to present data in a manner so that others can understand it we can arrange the dashboard to our liking.
> 4. On Sales in the South, right-click in the column area under the `Region `column header, and clear `Show` Header. Repeat the same for `Category` row header. This helps to show only what is needed and hiding the unnecessary information.
> 5. Right-click the `Profit Map` title and select `Hide Title`. Repeat the same for `Sales in the South` view.
> 6. Select the first `Sub-Category` filter card on the right side of your view, and at the top of the card, click the `Remove` icon. Repeat this step for the second `Sub-Category` filter card and one of the `Year of Order Date` filter cards. Click the drop-down arrow at the top of the `Year of Order Date` filter, and select `Single Value (Slider)`.Now let the magic unfold. Try selecting different years on the Year of Order Date filter and see how the data is quickly filtered to show that state performance varies year by year. 
> 7. Drag the `SUM(Profit)` filter and drag it at the bottom of the dashboard below Sales in South.

### `Hands On`
 
 ![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Dashboard/creating%20dashboard.gif)  
    


## Adding Interactiveness 

#### In order to make the dashboard more interactive like viewing which sub-categories are profitable in specific states, few changes need to be done.


### `Steps`

> 1. Select `Profit Map` in the dashboard, and click the `Use as filter` icon  in the upper right-hand corner
> 2. Now if we select any state in the map, the Sales in the `South chart` updates to show just the sub-category sales.
> 3. Select the `Year of Order Date` filter, click its drop-down arrow, and select `Apply to Worksheets > Selected Worksheets`.
> 4. In the `Apply Filter to Worksheets` dialog box, select `All` in the dashboard, and then click `OK`. This is done in order to apply the filter to all worksheets in the dashboard that use this same data source.
> 5. Now explore and experiment. In the viz. below we will filter `Sales in the South` to only items sold in North Carolina, and then explore year by year profit.
> 6. Rename the Dashboard to `Regional Sales and Profit`.


### `Hands On`
    
![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Dashboard/adding%20interactiveness.gif)   


#### **Thus, selling machines in the North Carolina did not bring any profits to the company.** 


# <a name="story"></a>6. Story

#### A dashboard is a cool feature but tableau also offers us to showcase our results in presentation mode in form of stories about which we will discuss in this section.

## Building a Story 

### `Steps`

> 1. Click the `New story` button.
> 2. From the Story pane on the left, drag the `Sales in the South` worksheet onto your view.
> 3. Edit the text in the gray box above the worksheet. This is the caption. Name it as `Sales and profit by year`.
> 4. Stories are quite specific. Here we will tell a story about selling machines in North Carolina. In the Story pane, click `Duplicate` to duplicate the first caption.
> 5. In the `Sub-Category`, filter `select` only `Machines`. This helps to gauge sales and profit of machines by year.
> 6. Rename the caption to `Machine sales and profit by year`.

### `Hands On`

![Alt Text](https://github.com/parulnith/Data-Visualisation-with-tableau/blob/master/%20images%20and%20gifs/Story/Buildign%20a%20story.gif)


## Making a Conclusion 

#### It is clear that machines in North Carolina is leading to loss of profit. However, this cannot be demonstrated by looking at Profit and Sales on the whole. For thi,s we need regional Profit.

### `Steps`
> 1. To see how Profit varies in North Carolina with years, simply Duplicate the Regional Profit dashboard focused on North Carolina.
> 2. Drag the dashboard `Regional Sales and Profit` onto the canvas.
> 3. Caption it as `Low performing items in the South`.
> 4. Select `Duplicate` to Create another story point with your Regional Profit dashboard. Select North Carolina on the bar chart.
> 5. Select All the years.
> 6. Add a caption, for example, `Profit in NC, 2014-2016`.
> 7. Select any year like 2014. Add a caption, for example, `Profit in NC, 2014` and then click Duplicate. Repeat the same for all the remaining years.



### `Hands On`

![Alt Text]()

#### Now we will have an idea of which products were introduced to the North Carolina market when, and how poorly they performed. Not only have we identified a way to address negative profit, but have also successfully managed to back it with data. This is the advantage of Story in Tableau.


# <a name="saving"></a>7. Saving the work

## Tableau Desktop 

To save a Tableau workbook locally,  Select File > Save. Specify the workbook file name in the `Save As `dialog box. Tableau saves the file with the .twb extension by default.

## Tableau Public
With Tableau Public all the views and data is made public and anybody on the internet has access to it. `Select Server > Tableau Public > Save to Tableau Public` and enter the credentials.

## [Tableau Server](https://www.tableau.com/products/server)
In case the data is confidential and the story needs to be shared with the entire team, Tableau Server comes in handy.To publish a story to Tableau Server,  Select `Select Server > Publish Workbook` or `click Share` on the toolbar. But make sure to create an account first.

---
### That's all we need to create a good visualization in Tableau although, one might find doing a lot more revising in each stage than we did here. So with experimentation and practise, tableau becomes a lot more familiar and will unleash amazing features to help us analyze and present data. Please comment below in case of any queries or questions and Happy Visualising. 
---
