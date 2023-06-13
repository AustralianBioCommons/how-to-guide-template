---
title: Testing your guides to improve content
type: guides
contributors: [Johan Gustafsson]
description: How to deploy and further enrich the content of your guides.
---


## Deploy to GitHub pages

To deploy your guide to GitHub pages:

1. Go to your repository `Settings`;
2. Select `Pages` from the left hand navigation menu;
3. In the `Source` drop-down menu select `Deploy from branch`;
4. In the `Branch` drop-down menu select `Main`; and,
5. Click `Save`

The documentation for GitHub provides additional information on how to [**set up GitHub pages for your repository**](https://pages.github.com/). Make sure to select the options `Project site` and `Start from scratch`: this will provide a straightforward walkthrough for setting up GitHub pages.


## Improve your How-to Guide

### Testing functional content

As an example, some How-to Guides detail the use of the bioinformatics platform Galaxy and demonstrate its application to analysis of real world data. It is critical that the functional content included (tools, workflows, code) is tested by:

- The original developer ( *if this isn't you* ); and 
- New users who have never seen the content before

A good example is a bioinformatics workflow: this workflow should be tested to ensure it functions as expected. This makes it more likely that someone will be able to successfully reuse the part of the guide that refers to the workflow.


### Make sure that others can understand your How-to Guide
 
The How-to Guide you create will be more reusable if multiple people have worked through the content. They will either successfully complete the activities in the guide, or provide critical feedback that can be used to improve the How-to Guide.


### Add links that import a workflow to Galaxy

You can embed links into a How-to Guide that instruct a Galaxy instance to import a specific version of a workflow from a source like [Dockstore](https://dockstore.org/) or [WorkflowHub](https://workflowhub.eu/). The example use case is if you would like a user of your guide to be able to open a workflow by simply clicking a link.

An example is included here for WorkflowHub:

```
https://usegalaxy.org.au/workflows/trs_import?trs_server=workflowhub.eu&trs_id=221&trs_version=3
```

Breaking the link down into its components:

1. `https://usegalaxy.org.au/workflows/trs_import`: [Galaxy Australia](https://usegalaxy.org.au/), please initiate a workflow import using my account
2. `?trs_server=workflowhub.eu`: use the [WorkflowHub TRS](https://about.workflowhub.eu/developer/trs/) server, and
3. `&trs_id=221&trs_version=3`: import workflow ID `221`, version number `3`

{% include callout.html type="important" content="A user needs to log in to Galaxy first for the workflow import to be successful." %}

If you add these links, don't forget to also cite the workflow. Example for the workflow used above:
> Price, G., & Farquharson, K. (2022). PacBio HiFi genome assembly using hifiasm v2.1. WorkflowHub. https://doi.org/10.48546/WORKFLOWHUB.WORKFLOW.221.3

 