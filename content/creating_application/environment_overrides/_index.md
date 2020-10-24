+++
bookCollapseSection = false
title = "Environment Overrides"
description = ""
weight = 7
+++



{{< figure src="./env_ride.jpg" height="410px">}}

&nbsp;&nbsp;

You can customize the Deployment template in Environment Overrides section to customize things according to multiple environments such dev, test, integration, prod, etc.


For Example, You may have specified 100m CPU resource in the Deployment Template but in Production environment override you may want to have 500m CPU resource as the traffic on Pod is higher than usual.

The changed configuration will not be added in the template, instead it will make a copy of the template and lets you customize it and then save it.
And now this overriden template will be used always for your Production Environment instead of the one specified in deployment template.

&nbsp;&nbsp;

![Environment Overrides](../../arora4.gif "Environment Overrides")
