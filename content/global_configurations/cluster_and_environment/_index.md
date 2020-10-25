+++
bookCollapseSection = false
title = "Cluster And Environments"
description = ""
weight = 3
+++

The Global configuration provides a feature of `Cluster & Environment` in which you can add your Kubernetes clusters and environment.

Select the Cluster & Environment section of global configuration and click on `Add Cluster` to add your cluster.

  

## Add Cluster:

Provide the below information to add your kubernetes cluster:

1.  Name
    
2.  Kubernetes Cluster Info
    

    -   Server URL
    
    -   Bearer token
    

3.  Prometheus Info
    

    -   Prometheus endpoint
    

        -   Basic
    

             -   Username
    
             -   Password
    

         -   Anonymous
    

    -   TLS Key
    
    -   TLS Certificate

&nbsp;&nbsp;

{{< figure src="../../cluster_gc1.png" height="470px">}}

&nbsp;&nbsp;

### 1. Name

Give a name to your cluster inside the name box.

  

### 2. Kubernetes Cluster Info

Provide your kubernetes cluster’s credentials.

  

-   **Server URL**
    

Provide the endpoint/URL of your kubernetes cluster.

-   **Bearer token**
    

Provide your kubernetes cluster’s Bearer token for authentication purposes so that the Devtron tool will be able to talk to your kubernetes cluster and can deploy your application in your kubernetes cluster.

  

### 3. Prometheus Info

Prometheus is a powerful solution to provide graphical insight into your application behavior. If you want to see your application matrix against your applications deployed in kubernetes, install Prometheus in your kubernetes cluster. The below inputs are required to configure your prometheus into Devtron’s tool.

-   **Prometheus endpoint**
    

Provide the URL of your prometheus. Prometheus supports two types of authentication `Basic` and `Anonymous`. Select the authentication type for your Prometheus setup.

  

-   **Basic**
    

If you select the `basic` type of authentication then you have to provide the `Username` and `Password` of prometheus for authentication.

  

-   **Anonymous**
    

If you select `Anonymous` then you do not have to provide any username and password for authentication.

  

-   **TLS Key & TLS Certificate**
    

TLS key and TLS certificate both options are optional, these options are used when you use a custom URL, in that case, you can pass your TLS key and TLS certificate.

  

Check the below screenshots to know how it looks like If you select the `Basic` authentication type

&nbsp;&nbsp;

{{< figure src="../../cluster_gc2.png" height="490px">}}

&nbsp;&nbsp;

If you select the `Anonymous` authentication type

&nbsp;&nbsp;

{{< figure src="../../cluster_gc3.png" height="470px">}}

&nbsp;&nbsp;

Now click on `Save Cluster` to save your cluster information.

  

### Note:

Your kubernetes cluster gets mapped with the Devtron when you save your kubernetes cluster Configuration. Now the agents of devtron will be installed on your cluster so that the components of devtron can communicate to your cluster. When the agent starts installing on your cluster, you can check the status of the agents in the Cluster & Environment tab also.

&nbsp;&nbsp;

{{< figure src="../../cluster_gc4.png" height="230px">}}

&nbsp;&nbsp;

Click on `Details` to check what got installed inside the agents. A new window will be popped up displaying all the details about these agents.

&nbsp;&nbsp;

{{< figure src="../../cluster_gc5.png" height="250px">}}

&nbsp;&nbsp;

## Add Environment

  

Once you have added your cluster in Cluster & Environment, you can add the environment also. Click on `Add Environment`, a window will be opened. Give a name to your environment in the `Environment Name` box and provide a namespace corresponding to your environment in the `Namespace` input box. Now choose if your environment is for Production purposes or for Non-production purposes. Production and Non-production options are only for tagging purposes. Click on `Save` and your environment will be created.

&nbsp;&nbsp;

{{< figure src="../../cluster_gc6.png" height="510px">}}

&nbsp;&nbsp;

## Update Environment

  

You can update an already created environment, Select and click on the environment which you want to update. You can only change Production and Non-production options here.

Note- you can not change the Environment name and Namespace name.

&nbsp;&nbsp;

{{< figure src="../../cluster_gc7.png" height="510px">}}

&nbsp;&nbsp;