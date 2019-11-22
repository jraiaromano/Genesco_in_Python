# Genesco_in_Python
## Overview
This is the repo for a class project in which I used Python to analyze sales data provided by Genesco. The task was to provide insights to drive sales strategy. 

## Project Takeaways
This data had Just So. Many. Columnss. 114 to be precise. Just an absolute mess to work with. With such a big dataset, melting and .query were my friends, as was pickling. It became very important to be able to group by... anything, really, in order to save processing time. 
## The Pitch
Comparative sales increase is the "holy grail of retail", and so our project partner wants to understand how well the metrics his company collects help explain the change in sales for a given week for one fiscal year compared to the same week for the previous fiscal year. Comparing sales for the same period in two consecutive years is a measure of growth for the company and provides value to shareholders.
Genesco would like us to answer the following questions:
- is the company measuring the right things?
- which metrics correlate most with comp sales increase?
- what measures either influence or help explain variations in comp increase

## The Data 
Metrics provided include employee metrics, foot traffic (measured by people exiting through the front door) and conversion rate (the percentage of customers who enter the store and make a purchase). The dataset includes a calculated measure STRAK_COMP_TRAFFIC_DELTA, which is the difference between the comparative sales percent and the foot traffic conversion rate. 
Stores report sales metrics daily, but they have been summed to weekly amounts in the provided dataset.

The fiscal year runs from February 1 to January 31, and the FY is for the ending year. For example FY2020 began on February 1, 2019 and will end January 31, 2020.
## Approach to the Problem
Originally, my team decided to break the dataset up into general sections: employee data, traffic data, and merchandise data. I was assigned merchandise data, particularly accessories... of whihc there were a solid 32 columns. I was able to melt them down to a couple, and was able to pull out a couple of weak correlations between traffic, sales, and certain types of accessories, but nothing groundbreaking. For example, it is became obvious that when a store is busy (large shopper/associate ratio) there was a low conversion rate but a high items per transaction ratio, accompanied by a higher sale-of-units of socks and belts. Clearly, shoppers enter stores, and either leave (low conversion) or shop for accessories until an associate is free to help them (high units/sale, high units of accessories). This is both easy to understand and not terribly unexpected. Further into the project, I began to break down the data by store type, as they all tended to funciton differently. Once I successfully did this, I was able to see some mild correlations between the comparative sales ratio and a couple metrics, including the ratio of shoes sold to accessories sold in the same transaction:
IMAGE OF PLOT
