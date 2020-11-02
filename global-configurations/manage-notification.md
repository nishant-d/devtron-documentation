# Manage Notification

his feature helps you manage the notifications for your build and deployment pipelines. You can receive the notifications on Slack or via e-mail.

Click on `Global Configurations` -&gt; `Notifications`

### Notification Configuration:

Click on `Configurations` and you will see Devtron support two types of configurations `SES Configurations` or `Slack Configurations`.

![](../images/global-configurations/manage-notification/not2.jpg)

#### **Manage SES Configurations**

You can manage the `SES configuration` to recieve e-mails by entering the valid credentials. Make sure your e-mail is verified by SES.

![](../images/global-configurations/manage-notification/not1.jpg)

Click on `Add` and configure SES.

![](../images/global-configurations/manage-notification/not3.jpg)



| Key | Description |
| :--- | :--- |
| `Configuation Name` | Give a name to the SES Configuration |
| `Access Key ID` | Valid AWS Access Key ID |
| `Secret Access Key` | Valid AWS Secret Access Key |
| `AWS Region` | Select the AWS Region from the drop-down menu |
| `E-mail` | Enter the SES verified e-mail id on which you wish to recieve e-mail notifications |

Click on `Save` to save your SES configuration or e-mail ID

#### **Manage Slack Configurations**

You can manage the `Slack configurations` to recieve notifications on your preferred Slack channel.

![](../images/global-configurations/manage-notification/not4.jpg)

Click on `Add` to add new Slack Channel.

![](../images/global-configurations/manage-notification/not5.jpg)



| Key | Description |
| :--- | :--- |
| `Slack Channel` | Name of the Slack channel on which you wish to recieve notifications. |
| `Webhook URL` | Enter the valid [Webhook URL link](https://slack.com/intl/en-gb/help/articles/115005265063-Incoming-webhooks-for-Slack) |
| `Project` | Select the project name to control user access |

Click on `Save` and your slack channel will be added.

### **Manage Notifications**

Click on `Add New` to recieve new notification.

![](../images/global-configurations/manage-notification/notifi7.jpg)

#### **Manage Slack Notifications**

![](../images/global-configurations/manage-notification/notifi6.jpg)



_**Send To**_

When you click on the `Send to` box, a drop-down will appear, select your slack channel name if you have already configured Slack Channel. If you have not yet configured the Slack Channel, Click on [Configure Slack Channel](manage-notification.md#manage-slack-configurations)

_**Select Pipelines**_

* Then, to fetch pipelines of an application, project and environment.
  * Choose a filter type\(`environment`, `project` or `application`\)
  * You will see a list of pipelines corresponding to your selected filter type, you can select any number of pipelines. For each pipeline, there are 3 types of events `Trigger`, `Success`, and `Failure`. Click on the checkboxes for the events, on which you want to receive notifications.

![](../images/global-configurations/manage-notification/not10.jpg)

Click on `Save` when you are done with your Slack notification configuration.

#### **Manage SES Notifications**

![](../images/global-configurations/manage-notification/notifi6.jpg)



_**Send To**_

* Click on the Send To box, select your e-mail address/addresses on which you want to send e-mail notifications. Make sure e-mail id are SES Verified.

If you have not yet configured SES, Click on [Configure SES](manage-notification.md#manage-ses-notifications)

_**Select Pipelines**_

* To fetch pipelines of an application, project and environment.
  * Choose a filter type\(environment, project or application\)
  * You will see a list of pipelines corresponding to your selected filter type, you can select any number of pipelines. For each pipeline, there are 3 types of events `Trigger`, `Success`, and `Failure`. Click on the checkboxes for the events, on which you want to receive notifications.

![](../images/global-configurations/manage-notification/not9.jpg)

Click on `Save` once you have configured the e-mail notification.
