---
title: Overview of Charts
weight: 1
---


# Deploying Charts

Charts can be deployed individually or by creating a group of Charts.

Both methods are mentioned in the given document.


## Deploying Chart

&nbsp;&nbsp;

{{< figure src="../../depchart1.JPG" height="380px">}}

&nbsp;&nbsp;

Select Discover and then select the chart that you want to use

<br />

Click on README.MD to get more idea about the configurations of the chart

<br />

{{< figure src="../../custom.jpg" height="430px">}}

<br />

Select the Chart Version that you want to use and Chart Value, you can either use the default Values or custom values.
To know about Custom Values, Click On: [Custom Values](https://docs.devtron.ai/docs/reference/deploy-chart/overview/#custom-values)

<br />


The configuration values can be edited in the section given below Chart Version.

Key | Description
----|----
`App Name` | The name of the app
`Project` | Project of the app
`Environment` |Environment of the app to be deployed
`Chart Version` | Version of the chart to be used

&nbsp;&nbsp;

{{< figure src="../../depchart4config.JPG" height="390px">}}

&nbsp;&nbsp;

ReadMe.md present on the left can be used by the user to set configuration values

&nbsp;&nbsp;

{{< figure src="../../depchart4readme.JPG" height="390px">}}

<br />

Click on `Deploy Chart` to deploy the chart

&nbsp;&nbsp;

{{< figure src="../../depchartdeployedredo.JPG" height="390px">}}

&nbsp;&nbsp;

You can see the status of the chart deployed. Click on `Values.Yaml` to reconfigure the deployment.

&nbsp;&nbsp;

{{< figure src="../../depchartreconfig.JPG" height="390px">}}

&nbsp;&nbsp;

Configuration values can be edited over here by the help of ReadMe.md

Select Update And Deploy to update new settings.

##  Custom Values

You can use the default values or create Custom value by clicking on ` Create Custom`

&nbsp;&nbsp;

{{< figure src="../../custom.jpg" height="430px">}}

&nbsp;&nbsp;

You can name your Custom Value, select the Chart Version and change the configurations in YAML file.

&nbsp;&nbsp;

{{< figure src="../../custom_val.jpg" height="510px">}}

&nbsp;&nbsp;

Click on `Save Template` to save the configurations.



## Deploying Chart Groups 

To deploy multiple applications and work with them simulataneously, you can use `Chart Groups`.

To create Chart Groups 
Click on  `Discover` and Click on `Create Group`

&nbsp;&nbsp;

{{< figure src="../../screen2.jpg" height="420px">}}

&nbsp;&nbsp;

Add the Group Name and Description and Click on `Create Group`

&nbsp;&nbsp;

{{< figure src="../../create_group.jpg" height="440px">}}

&nbsp;&nbsp;

You can select the Charts that you want to add in your Chart Group by clicking on '+' sign. 
You can select a particular chart multiple number of times according to your requirements.

&nbsp;&nbsp;

{{< figure src="../../select_charts.jpg" height="430px">}}

<br />

Select the `Version` and `Values` for your charts.

You can use Default Values or the Custom Values, just make sure the Value that you select for your Chart is comptabile with the Version of the Chart that you are using.

&nbsp;&nbsp;

{{< figure src="../../select_charts2.jpg" height="430px">}}

&nbsp;&nbsp;

To edit the Chart Configuration, Click on 'Edit'

&nbsp;&nbsp;

{{< figure src="../../edit_group.jpg" height="430px">}}

&nbsp;&nbsp;

You can `Add` more Charts to your existing Chart Group or `Delete` Charts from your existing Chart Group. 

After making changes, Click on `Save` to save changes to your Chart Group.

&nbsp;&nbsp;

{{< figure src="../../edit_group2.jpg" height="430px">}}

&nbsp;&nbsp;

If you wish to edit the Chart Configuration, Double Click on that Chart and edit the Configurations in YAML File.

&nbsp;&nbsp;

{{< figure src="../../edit_chart1.jpg" height="430px">}}

&nbsp;&nbsp;

You can edit the `App Name`, `Chart Version`, `Values`, `Deploy Environment` and the YAML file.

&nbsp;&nbsp;

Key | Description
----|----
`App Name` | Name of the app
`Project` | Name of Project in which app has to be created
`Environment` | Name of the Environment in which app has to be deployed
`Chart Version` | Select the Version of the chart to be used

<br />

Click on `Deploy` to initiate the deployment of a Chart in Chart Group.
