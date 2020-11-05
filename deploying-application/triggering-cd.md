# Triggering CD

### Triggering CD Pipelines

![](../images/deploying-application/triggering-cd/trigger-select-image.jpg)

After CI Pipeline is complete, CD Pipeline can be triggered by Clicking on _Select Image_.

![](../images/deploying-application/triggering-cd/cd-deploy-console.jpg)

Select an image to deploy and then Click on **Deploy** to trigger the CD Pipeline.

The running images are tagged as _Running_

![](../images/deploying-application/triggering-cd/deployed-app-details.jpg)

The status of the current deployment can be viewed by Clicking on **App Details** that will show the _Progressing_ state for 1-2 minutes and then gradually shows _Healthy_ state or _Hibernating_ state, based on the deployment strategy.

Here, triggering CD Pipeline is successful and the deployment is in "Healthy" state.

[To further diagnose deployments, Click here](../debugging-deployment-and-monitoring.md)
