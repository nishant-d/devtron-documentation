---
title: Triggering CI
weight: 1

---

## Triggering CI Pipelines

&nbsp;&nbsp;

{{< figure src="../../tri_ci.jpg" height="340px">}}

&nbsp;&nbsp;

The CI Pipeline can be triggered by selecting **Select Material**

CI Pipelines that are set as Automatic are always triggered as soon as a new commit is made to the git branch they're sensing. However, CI Pipelines can always be manually triggered as and if required.

&nbsp;&nbsp;

{{< figure src="../../tri_ci2.jpg" height="490px">}}

&nbsp;&nbsp;

Various commits done in the repository can be seen, here along with details like Author, Date etc.
Select the commit that you want to trigger and then select "Start Build" to trigger the CI Pipeline.

<br />

**Refresh** icon, refreshes Git Commits in the CI Pipeline and fetches the latest commits from the “Repository”  

**Ignore Cache** : This option will ignore the previous build cache and create a fresh build. If selected, will take a longer build time than usual.

&nbsp;&nbsp;

{{< figure src="../../tri_ci3.jpg" height="320px">}}

&nbsp;&nbsp;

It can be seen that the pipeline is triggered here and is the *Running* state.

Click on your **CI Pipeline** or Click on **Build History** to get the details about the CI Pipeline such as logs, reports etc.

&nbsp;&nbsp;

{{< figure src="../../tri_ci5.jpg" height="420px">}}

&nbsp;&nbsp;

You can read the **logs** of the CI Pipeline from here.

&nbsp;&nbsp;

{{< figure src="../../tri_ci6.jpg" height="350px">}}

&nbsp;&nbsp;

Click on **Source code** to view the details such as commit id, Author and commit message of the Git Material that you have selected for the build.

&nbsp;&nbsp;

{{< figure src="../../tri_ci4.jpg" height="350px">}}

<br />


Click on **Artifacts** to download the *reports* of the Pre-CI and Post-CI stages if any.

<br />
