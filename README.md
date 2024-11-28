# kovai.co
  Power BI is a Business Intelligence tool which can be used for creating interactive dashboards using the data.  Data can be imported or exported from the PowerBI. 
Forecasting can also be done using Power BI exponential smoothening algorithm.
Forecasting in Power BI will help us to predict the future based on our current information. Forecast in Power BI can be done by following some simple steps.

Requirements to forecast data in Power BI
First, Install the Power BI Desktop.
Secondly, Install SQL Server.

Steps:
First, in Power BI press the Get data option.
forecast data in power bi - get data

Secondly, select the SQL Server database option and press Connect.
forecast data in power bi - SQL Server source

Thirdly, write the SQL Server name. In my case, I am using the local server. Press OK.
forecast data in power bi - sql server connection properties

Also, in the Adventureworks database, check the Purchasing.PurchaseOrderDetail table. 

Visualize the data to forecast
First, check the Purchasing.PurchaseOrderDetail table and the Year. Also, check the OrderQty field.

Select fields
Secondly, select the Line chart. Make sure that the DueDate Year in the X-axis and the Y-axis have the Sum of OrderQty.

Select the line chart
If everything is OK, the chart will be displayed.

forecast data in power bi - forecast chart created
Further analyses of your visual
To enable the forecast option, select add further analyses to your visual icon and then turn on the Forecast option. Note that the forecast option is not available if Power BI does not detect dates in the chart. If Power BI does not detect dates in the fields used, by the chart, you will not see the forecast option.

Forecast option
The Forecast includes the following options.
First, we have units. Units are used to find if we want to forecast in Years, Quarters, Days or whatever option is available for the time.
Secondly, we have Forecast Length. It is used to configure how many units ahead do we want to forecast. By default, the number is 10. In this example, we are using the Forecast length equal to 10, which means that we will forecast 10 years.
Thirdly we have the Ignore the last option. It is useful when you think that some intervals of time should not be included in the forecast analysis because they are not representative. For example, if we had great sales before the COVID pandemic and during the pandemic, we have bad years. We think our forecast should not include the last 2 years because we are optimistic.
Also, we have Seasonality. It is an option in Power BI. The option is used to determine some tendencies at a certain time. It will detect certain variations during the year. This option could be used to determine some patterns in the information and make some predictions about the future. For example, we can detect more sales during winter or during summer. Some valid values for seasonality are yearly, quarterly, monthly, weekly, and daily.
Finally, we have the Confidence interval. This is a percentage used to determine how confident the value is. It is a range of values of the forecasted value. We consider this as the forecasting value with a margin of error. This margin is set by the user.
forecast properties
forecast data in power bi - forecast values
Upper bound and Lower bound values
If you move the mouse over the lines in the chart, you will notice that the line has 3 values:
First, you have the Forecast value which is the estimated value.
Secondly, you have the Upper bound which is the maximum forecast value.
Finally, you have Lower bound which is the minimum forecast value. Both, the upper bound and lower bound are determined by the Confidence interval explained previously.
forecast data in power bi - upper bound lower bound

chart forecast

Forecast data in Power BI – Changing the format
Follow these steps to change the forecast format in Power BI:

First, press add further analyses to your visual icon.

Secondly, look for the Forecast line.

Forecast line

You have 3 options here:

First, you have the color which is used to change the color of the forecast line.
Secondly, you have a style that can be dotted, solid, or dashed.
Finally, you can configure the transparency of the forecast colors.
format options

In addition, you can configure the Confidence band. By default, you fill in, but you can use lines or remove the confidence band using the none option. Finally, you have the option to modify the tooltip title of the forecast value.

Confidence band

Forecast data in Power BI
Sometimes you need to see the values instead of watching the chart only. To check a table instead of a chart, you can follow these steps:

First, click on the More options icon.

Secondly, select the Show as a table option.

Finally, you will be able to see in a table the ForecastValue, the confidence Hight Bound and Low Bound values which were explained previously.
