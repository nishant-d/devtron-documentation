---
title: Deploying mySQL Helm chart
weight: 3
---


# Deploying mySQL Helm chart


## Introduction 

stable/mysql Helm chart bootstraps a single node MySQL deployment on a Kubernetes cluster using the Helm package manager.

&nbsp;&nbsp;

![Helm Chart](../../../mysql.jpg )

&nbsp;&nbsp;

## 1. Discover the chart from the Chart Store

Select the `Charts` section from the left pane, you will be landed to the `Chart Store` page. Click on `Discover` and find `stable/mongodb-replicaset` Helm Chart.

&nbsp;&nbsp;
![Helm Chart](../../../chart21.jpg "Deploying Chart")

&nbsp;&nbsp;

## 2. Configure the Chart

After selecting the stable/mySQL Helm chart, click on `Deploy` 

<br />

Enter the following details, to deploy mysql chart:

<br />

Key        | Description
-----------|-------------
`App Name` | Name of the Chart
`Project` | Select the name of your Project in which you want to deploy the chart
`Environment` | Select the environment in which you want to deploy the chart
`Chart Version` | Select the latest Chart Version
`Chart Value` | Select the latest default value or create a custom value

&nbsp;&nbsp;

### Configure `values.yaml` 

Set the following parameters in the chart, to be later used to connect mysql with your Django Application.

&nbsp;&nbsp;

![Helm Chart](../../../chart3.jpg "Deploying Chart")

&nbsp;&nbsp;

Parameters     | Description
---------------|-------------
`mysqlRootPassword` | Password for the root user. Ignored if existing secret is provided
`mysqlDatabase` | Name of your mysql database
`mysqluser`     | Username of new user to create
`mysqlPassword` | Password for the new user. Ignored if existing secret is provided

&nbsp;&nbsp;

![Helm Chart](../../../chart4o.jpg "Deploying Chart")
&nbsp;&nbsp;
Click on `Deploy` to deploy the Chart 

<br />

## 3. Check the Status of Deployment

After clicking on `Deploy` you will land on a page, that shows the Status of the deployment of the Chart. 

The Status of the chart should be `Healthy`. It might take few seconds after  initiating the deployment of the chart.

&nbsp;&nbsp;

![Create Group](../../../sql1.png  "Create Groups")

&nbsp;&nbsp;

In case the Status, of the deployment is `Degraded` or takes a long time to get deployed. 

Click on the `Status` or check the logs  of the pods to debug the issue.



## 4. Extract the Service Name

Copy the service name, it will be used to connect your application to mySQL.

&nbsp;&nbsp;

![Create Group](../../../sql2.png  "Create Groups")

&nbsp;&nbsp;
