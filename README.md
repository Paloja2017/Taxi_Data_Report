# **Taxi Travel Power BI Report**

![](TaxiPhoto.jpg)

## Introduction

Microsoft last couple of month has released a public preview of **Microsoft Fabric**. Me as Power BI developer and tech enthusiast I started to experiment with it and I thought maybe it is very good to document as the project on GitHub also for my protfolio. This was the starting point, the project was quite simple, the main thing I wanted to experiment with was Taxi Data as sample data which is almost 160 milion rows and the connection as Direct lake.

## Problem statement

Simulation:
Fictive **Taxi** company want to implement new **Microsoft Fabric** capabilities to their BI analysis. They want real time data analysis so we have agreed to use Microsoft Direct Lake as storage in Power BI.
  
## Requirements

Simulate the client **Taxi** Company requirement of measuring these metrics:
- Fare Amount Value
- Total Amount Value
- Tip Amount Value
- Count of trips
- Average Trips Amount

These metrics should be compared on calendar base year, month, day. -I havent gone to deeper analysis of hour, minute, most frequent hours of the day-
  
## Skills demonstrated

As I mention project is quite simple, some of the skills shown in this project are field parameters, card highlighting when same measure is clicked, UI appearance... Usage of field parameters was ment to use the same visual interface to measure different metrics. Of course we can apply drillthough to another page and use tooltips for additional information.
## Project Steps

- Created a new workspace named Fatjan Paloja Fabric_Test and select a trial of Microsoft Fabric for 60 day.
 ![](Workspace_settings.png)

- Created a lake house
 ![](LakeHouse.png)
- Data source - Add new Data pipeline - TaxiDataPipeline_Directlake
![](PipelineData.png)
- Load to Delta table data preview
  ![](DeltaTablePreview.png)

- Link a Pipeline to Outlook and Teams - on data refresh succes they sent a mesage you write for example "Data is refreshed succesfully"
  ![](PipelinetoTeams.png)

- Data Transformation
- Created a View and added transformed date time column to date only
  ![](SQl_endpoint.png)

- Modeling Connected Power BI desktop to Onelake data hub - LakeHouses preview and loaded data as Direct lake and for calendar table I used SqlBI Bravo tool which has builded for me Calendar Table with DAX (You can use a Calendar Table builded in Dataflow Gen2 also). I have created relationship between Calendar Table and Taxi data on Date columns
![](DataModel.png)
- Analysis & visualizations
- Conclusion and recommendation

