+++
bookCollapseSection = false
title = "Manage Notification"
description = ""

weight = 6
+++


This feature helps you manage the notifications for your build and deployment pipelines. You can receive the notifications on Slack or via e-mail.

Click on `Global Configurations` -> `Notifications`

## Notification Configuration:

Click on `Configurations` and you will see Devtron support two types of configurations `SES Configurations` or `Slack Configurations`.

&nbsp;&nbsp;

{{< figure src="../../not2.jpg" height="410px">}}

&nbsp;&nbsp;

### **Manage SES Configurations**

You can manage the `SES configuration` to recieve e-mails by entering the valid credentials. Make sure your e-mail is verified by SES. 

&nbsp;&nbsp;

{{< figure src="../../not1.jpg" height="350px">}}

<br />

Click on `Add` and configure SES.

&nbsp;&nbsp;

{{< figure src="../../not3.jpg" height="520px">}}

&nbsp;&nbsp;

Key | Description
----|----
`Configuation Name` | Give a name to the SES Configuration 
`Access Key ID` | Valid AWS Access Key ID
`Secret Access Key` | Valid AWS Secret Access Key
`AWS Region` | Select the AWS Region from the drop-down menu 
`E-mail`     | Enter the SES verified e-mail id on which you wish to recieve e-mail notifications

Click on `Save` to save your SES configuration or e-mail ID

&nbsp;&nbsp;

### **Manage Slack Configurations**

You can manage the `Slack configurations` to recieve notifications on your preferred Slack channel.

&nbsp;&nbsp;

{{< figure src="../../not4.jpg" height="170px">}}


<br />

Click on `Add` to add new Slack Channel.

&nbsp;&nbsp;

{{< figure src="../../not5.jpg" height="450px">}}

&nbsp;&nbsp;

Key | Description
----|----
`Slack Channel` | Name of the Slack channel on which you wish to recieve notifications.
`Webhook URL` | Enter the valid [Webhook URL link](https://slack.com/intl/en-gb/help/articles/115005265063-Incoming-webhooks-for-Slack) 
`Project` | Select the project name to control user access

Click on `Save` and your slack channel will be added.

&nbsp;&nbsp;

## **Manage Notifications**

Click on `Add New` to recieve new notification.

&nbsp;&nbsp;

{{< figure src="../../notifi7.jpg" height="420px">}}

&nbsp;&nbsp;

### **Manage Slack Notifications**

&nbsp;&nbsp;

{{< figure src="../../notifi6.jpg" height="410px">}}

&nbsp;&nbsp;

***Send To***

When you click on the `Send to` box, a drop-down will appear, select your slack channel name if you have already configured Slack Channel. If you have not yet configured the Slack Channel, Click on [Configure Slack Channel](/global_configurations/manage_notification/#manage-slack-configurations)

<br />

***Select Pipelines***

* Then, to fetch pipelines of an application, project and environment.

   * Choose a filter type(`environment`, `project` or `application`)

   * You will see a list of pipelines corresponding to your selected filter type, you can select any number of pipelines. For each pipeline, there are 3 types of events `Trigger`, `Success`, and `Failure`. Click on the checkboxes for the events, on which you want to receive notifications. 

&nbsp;&nbsp;

{{< figure src="../../not10.jpg" height="580px">}}

<br />

Click on `Save` when you are done with your Slack notification configuration.

<br />

### **Manage SES Notifications**

&nbsp;&nbsp;

{{< figure src="../../notifi6.jpg" height="410px">}}

&nbsp;&nbsp;

***Send To***

* Click on the Send To box, select your e-mail address/addresses on which you want to send e-mail notifications. Make sure e-mail id are SES Verified.

If you have not yet configured SES, Click on [Configure SES](/global_configurations/manage_notification/#manage-ses-notifications)


<br />

***Select Pipelines***

* To fetch pipelines of an application, project and environment.

   * Choose a filter type(environment, project or application)

   * You will see a list of pipelines corresponding to your selected filter type, you can select any number of pipelines. For each pipeline, there are 3 types of events `Trigger`, `Success`, and `Failure`. Click on the checkboxes for the events, on which you want to receive notifications. 

&nbsp;&nbsp;

{{< figure src="../../not9.jpg" height="610px">}}

<br />

Click on `Save` once you have configured the e-mail notification.
