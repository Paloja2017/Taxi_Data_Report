
# **NYC Fast Taxis Company**
## **NYC Fast Taxis Company Power BI Report**

![](TaxiPhoto.jpg)
---
**Document Author**                                                   
|Date |Author|Version|Role|                   
|:----|:-----|:------------|:----|                                        
|08/01/2023|Fatjan Paloja| 1.0| Power BI Consultant 
## Introduction

Microsoft last couple of month has released a public preview of **Microsoft Fabric**. Me as Power BI developer and tech enthusiast I started to experiment with it and I thought maybe it is very good to document as the project on GitHub for my protfolio. This was the starting point, the project was quite simple, the main thing I wanted to experiment with was Taxi Data as sample data which is almost 160 milion rows, the connection as Direct lake and PowerBI desktop mixed mode (Direct query to AS and Import)

**_Datasets, model and report are not representing any real company or real data_**

## Statement

Simulation:
Fictive **Taxi** company want to implement new **Microsoft Fabric** capabilities to their BI analysis. They want real time data analysis so we have agreed to use Direct Query over AS and import as storage mode in Power BI.
  
## BI Requirements

Simulate the client **Taxi** Company requirement of measuring these metrics:
- Fare Amount Value
- Total Amount Value
- Tip Amount Value
- Count of trips
- Average Trips Amount

These metrics should be compared on calendar base year, month, day.
<br />
_I havent gone to deeper analysis of hour, minute, most frequent hours of the day_
  
## Skills demonstrated

As I mention project is quite simple, some of the skills shown in this project are field parameters, card highlighting when same measure is clicked, UI appearance... Usage of field parameters was ment to use the same visual interface to measure different metrics. Of course we can apply drillthough to another page and use tooltips for additional information.
## Project Steps

- Created a new workspace named Fatjan Paloja Fabric_Test and select a trial of Microsoft Fabric for 60 day.
  <br />
  <br />
 ![](Workspace_settings.png)

- Created a lake house
  <br />
  <br />
 ![](LakeHouse.png)
- Data source
  <br />
  Add new Data pipeline - TaxiDataPipeline_Directlake
  <br />
  <br />
![](PipelineData.png)
- Load to Delta table data preview
  <br />
  <br />
  ![](DeltaTablePreview.png)

- Link a Pipeline to Outlook and Teams - on data refresh succes they sent a mesage you write for example "Data is refreshed succesfully"
  <br />
  <br />
  ![](PipelinetoTeams.png)
  <br />
  <br />
- On SQL Endpoint I created a View and added new date only column
  <br />
  <br />
  ![](SQl_endpoint.png)

- Model view of storage mode as Datalake
  <br />
  <br />
   ![](DirectLakePicture.png)
  <br />
  <br />

- Modeling
  <br />
  Connected Power BI desktop to Onelake data hub - LakeHouses preview and loaded data as Direct Query over AS and for calendar table I used SqlBI Bravo tool which has builded for me Calendar Table with DAX (You can use a Calendar Table builded in Dataflow Gen2 also). I have created relationship between Calendar Table and Taxi data on Date columns
  <br />
  <br />
![](DataModel.png)

- Measures, Calculated Table and Field Parameter
  <br />
  I have used VertiPaq Analyzer to list the measures for showing here. The procedure is open the DaxStudio in Power BI external tools, in advanced tab export metrics, then connect Vertipaq Analyzer to connect to .vpax file.
  <br />
  <br />
  ![](Measures.png)

## Analysis & visualizations

  The report is single paged and intended for simplicity of usage. We are measuring five metrics: Fare Amount, Average Trips Amount, Number of Trips, Tip Amount and Total Amount in single page - you can change the metrics in slicer down right also we have a slicer down left for years you want to analyze.
When you click a particular metrics slicer down right that BAN number which is measured is highlighted.
  <br />

  ![](GifTest.gif)
    <br />
    
Interact with report 
![Taxis Company](https://img.shields.io/badge/Taxis%20Company-Power%20BI%20Report-ffbe0b?labelColor=7B88BF&style=flat&logo=PowerBI&logoColor=Yellow)

 
- Conclusion and recommendation

