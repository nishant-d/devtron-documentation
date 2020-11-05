<p align="center">Devtron is an open source software delivery workflow for kubernetes written in go.
<br>
<br>
<a href="https://devtron.ai/">Website</a>
·
<a href="https://devtron.ai/blog/">Blog</a>
·
<a href="https://discord.gg/72JDKy4">Join Discord</a>
·
<a href="https://twitter.com/DevtronL">Twitter</a>
</p>

## Why Devtron?
It is designed as a self-serve platform for operationalizing and maintaining applications (AppOps) on kubernetes in a developer friendly way. 
<br>
<br>
<img src="./preview.gif">
<br>
<br>
### Some of the benefits  provided by devtron are: 

#### Zero code software delivery workflow
- Workflow which understands the domain of **kubernetes, testing, CD, SecOps** so that you dont have to write scripts
- Reusable and composable components so that workflows are easy to contruct and reason through

#### Multi cloud deployment 
 - deploy to multiple kubernetes cluster
 - test on aws cloud 
   > coming soon: support for GCP and microsoft azure  

#### Easy dev-sec-ops integration
 
- Multi level security policy at global, cluster, environment and application for efficient hierarchical policy management
- Behavior driven security policy
- Define policies and exception for kubernetes resources
- Define policies for events for faster resolution


#### Application debugging dashboard
 
- One place for all historical kubernetes events 
- Access all manifests securely for eg secret obfuscation 
- ***Application metrics*** for cpu, ram, http status code and latency with comparison between new and old 
- ***Advanced logging*** with grep and json search 
- Intelligent ***correlation between events, logs*** for faster triangulation of issue 
- Auto issue identification 

#### Enterprise Grade security and compliances
 
- Fine grained access control; control who can edit configuration and who can deploy.
- Audit log to know who did what and when
- History of all CI and CD events
- Kubernetes events impacting application
- Relevant cloud events and their impact on applications
- Advanced workflow policies like blackout window, branch environment relationship to secure build and deployment pipelines

#### Gitops aware
 
- Gitops exposed through API and UI so that you dont have to interact with git cli
- Gitops backed by postgres for easier analysis
- Enforce finer access control than git

#### Operational insights
 
- Deployment metrics to measure success of agile process. It captures mttr, change failure rate, deployment frequency, deployment size out of the box.
- Audit log to understand the failure causes
- Monitor changes across deployments and revert easily



## Compatibility notes

- Only AWS kubernetes cluster is supported as of now
- It uses modified version of [argo rollout](https://argoproj.github.io/argo-rollouts/).
- application metrics only works for k8s 1.16+

## Community

Get updates on Devtron's development and chat with the project maintainers, contributors and community members.

 - Join the [Discord Community](https://discord.gg/72JDKy4) 
 - Follow [@DevtronL on Twitter](https://twitter.com/DevtronL)
 - Raise feature requests, suggest enhancements, report bugs at [GitHub issues](https://github.com/devtron-labs/devtron/issues)
 - Read the [Devtron blog](https://devtron.ai/blog/)


## Contribute

Check out our [contributing guidelines](CONTRIBUTING.md). Included are directions for opening issues, coding standards, and notes on our development processes.

## Vulnerability Reporting

We at Devtron take security and our users' trust very seriously. If you believe you have found a security issue in Devtron, please responsibly disclose by contacting us at security@devtron.ai.

## License

Devtron is available under the [Apache License, Version 2.0](LICENSE)

