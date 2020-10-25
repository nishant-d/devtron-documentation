---
title: Triggering CD
weight: 2
---

## Triggering CD Pipelines

&nbsp;&nbsp;

{{< figure src="../../tri_cd.jpg" height="340px">}}

&nbsp;&nbsp;

After CI Pipeline is complete, CD Pipeline can be triggered by Clicking on 
*Select Image*.

&nbsp;&nbsp;

{{< figure src="../../CD1.JPG" height="340px">}}

&nbsp;&nbsp;

Select an image to deploy and then Click on **Deploy** to trigger the CD Pipeline.

The running images are tagged as *Running*

&nbsp;&nbsp;

{{< figure src="../../tri_cd5.jpg" height="380px">}}

&nbsp;&nbsp;

The  status of the current deployment can be viewed by Clicking on **App Details** that will show the *Progressing* state for 1-2 minutes and then gradually shows *Healthy* state or *Hibernating* state, based on the deployment strategy.

Here, triggering CD Pipeline is successful and the deployment is in "Healthy" state.


[To further diagnose deployments, Click here](/debugging_deployments_and_monitoring/)
