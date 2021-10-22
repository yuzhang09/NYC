# NYC-Parking-and-Camera-Violations
## STA9760-Project01
## Introduction 
The dataset "The Open Parking and Camera Violations(OPCV)" is published at NYC OpenData, and it loaded with all parking and camera violations in NYC from 2016. In this project, I used Socrata API to connect to the OPCV API, and load xxx rows of data into an ElasticSearch instance with AWS, and do the visualization with Kibana. 

## Code 
My code is written in python and it is in src folder and named "main.py". First, I install and import all of the require libraries and packages, and I set up the evniroment variables, and use argparse to add arguments "page_size" and "num_pages". Next, I connect to the data source and Elastic Search with Sodapy and Requests modules. I set 1 shards with 1 replicas, and I list the fields with their types that are useful. Then, I use a if statement to check if the "num_pages" exists. If there is no "num_pages" in the command line, then load number of "page_size" rows and upload to es. Otherwise, it would load "num_pages"x"page_size" rows and upload to es, which I write a for loop to achieve it.

## Visualization
I use Kibana to make graphs. The first graph is 
