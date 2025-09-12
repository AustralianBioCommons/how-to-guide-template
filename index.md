---
title: Creating a How-to Guide
sidebar: false
toc_depth: 2
---

This guide describes *How-to* create new How-to Guide websites using a GitHub repository template. 

**What are How-to Guides?** They are step-by-step guides that support the reuse of bioinformatics tools, workflows and data on Australian compute systems and infrastructure.

The steps outlined below aim to:
- Reduce the time you spend creating guides by providing a standard structure to develop and maintain guidance material;
- Provide further guide templates for common use cases of the How-to Guides concept;
- Allow you to easily deploy these guides using GitHub pages and a remote theme provided by ELIXIR; and,
- Allow linking to Zenodo and creation of DOIs for each release. You created the content, others should be able to cite it!


## 1. Fork the template repository

Fork [**the template repository available at this link**](https://github.com/AustralianBioCommons/guide-template) to create a new repository in your GitHub account or organisation.


## 2. Understand the repository structure

The repository has the following directories and files:

| Directory / file    | Description                                                                                                                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `_data`             | Directory containing sidebar configuration files (e.g. `/_data/sidebars/main.yml`) as well as `affiliations.yml` and `CONTRIBUTORS.yml` which contain important metadata for the guide.                                       |
| `_sass`             | Directory for all `*.scss` files: you should not need to modify these files, unless you wish to change the theme (colours or structure).                                                                                      |
| `assets`            | Directory for core image files (i.e. `/assets/img`) used by the remote theme.                                                                                                                                                 |
| `pages`             | Directory where all guide content pages should be stored: new directories can be added as needed within `/pages`.                                                                                                             |
| `images`            | Directory for all images included in the guides.                                                                                                                                                                              |
| `_config.yml`       | Main configuration file which specifies high level metadata, the remote theme being used, and any optional settings required.                                                                                                 |
| `CITATION.CFF`      | A citation file format (CFF) file, which is a standard way of representing citation metadata and which can be included in GitHub repositories to provide guidance for others on how-to-cite your repository and its contents. |
| `contributors.md`   | A page that lists all contributors to the repository: i.e. those listed in `CONTRIBUTORS.yml`.                                                                                                                                |
| `index.md`          | The landing page for the web pages deployed from the repository: contains general information, how-to-cite information, acknowledgements and references.                                                                      |
| `LICENSE`           | A license file.                                                                                                                                                                                                               |
| `README.md`         | The README for the GitHub repository, which contains general information describing the contents of the repository.                                                                                                           |


## 3. Choose between a single or multi-page guide structure

The default repository is configured for a single page guide (`index.md`), as well as an `About` page (`about.md`) that can be used for additional information such as citation instructions, acknowledgements, and references. Navigation between these pages uses the buttons in the top navigation bar.

However, it is possible, and relatively straightforward, to modify the repository to allow for:

- Multiple pages with a navigation bar on the left hand side,
- Multiple distinct left hand navigation panels that help a user navigate to unique sets of pages, with the top navigation bar used to toggle between these sets of pages.

{% include section-navigation-tiles.html col = "2" custom = "option-2"%}


## 4. Updates for a single page guide

For a single page How-to Guide all of your content (i.e. the information or guidance you would like to share) should be added to `index.md`.


### Updating the main How-to Guide page: index.md

1. Open `index.md`
2. Add content to this file 
3. Option: use an existing template for the markdown content to make your life easier: see [page templates section](#page-templates). Don't forget to include the yaml header content (see below)
4. Update the yaml header content. 
   - You need to add a `title`, 
   - You may also add `contributors`, a `description` and `affiliations`

```yaml
---
title: [How-to Guide template]
contributors: [Johan Gustafsson]
description: Add a plain text description here.
affiliations: [Australian BioCommons]
---   
```

{:start="5"}
5. If you have added contributors or affiliations proceed to the next step and update [additional files](update_other_files)


### Page templates

The template repository already contains some example structures that can be used for the content of `index.md`, and include:

- [Standard page that can be used as a starting point for any type of guide](https://australianbiocommons.github.io/guide-template/example_page)
- [Suggested structure for a guide describing how to use a bioinformatics workflow](https://australianbiocommons.github.io/guide-template/example_bioinformatics_workflow_page)
- [Suggested structure for documentation describing a workflow: based on Australian BioCommons documentation guidelines](https://australianbiocommons.github.io/guide-template/example_workflow_documentation_page)

To use any of these examples, simply copy the markdown content from the relevant example file into the `index.md` file in your repository.

{% include callout.html type="tip" content="You can also build custom markdown down content using tools like [readme.so](https://readme.so/)." %}


## 6. Updating `CONTRIBUTORS.yml`

Every time you add a contributor  to an individual page (step 4 in a [single page](https://australianbiocommons.github.io/how-to-guide-template/add_single_page) or [multi-page](https://australianbiocommons.github.io/how-to-guide-template/add_new_pages) guide), you need to update the `CONTRIBUTORS.yml` file, which can be found in the `/data` directory.

This ensures that the added contributor:

1. Has their name included on each guide page where it has been added to the yaml header, and
2. Is provided with a tile in the Contributors section on the `about.md` page

The text you add to `CONTRIBUTORS.yml should be in this format:

```yaml
Firstname Lastname:
    git: github_username
    orcid: 0000-1234-5678-9012
    role: users_role
    affiliation: declared affiliation (not linked)
```


## 7. Updating `affiliations.yml`

Every time you add a new affiliation  to an individual page (step 4 in a [single page](https://australianbiocommons.github.io/how-to-guide-template/add_single_page) or [multi-page](https://australianbiocommons.github.io/how-to-guide-template/add_new_pages) guide), you need to update `affiliations.yml`, which can be found in the `/_data` directory. 

If you use affiliations in the yaml header content of any page, this will require this specific affiliation information to be available. 

A new example affiliation is available below: note that it also includes an image / logo which should be added to the `/images` directory.

```yaml
- name: Galaxy Australia
  image_url: /images/infrastructures/galaxy-aust-logo-portrait-CMYK.png
  expose: true
  type: infrastructure
  url: https://usegalaxy.org.au/
```

{% include callout.html type="note" content="You can add logos to the `/images` directory." %}


The [about.md](https://github.com/AustralianBioCommons/guide-template/blob/132851cbc0bb112cafbaa623487e4524af5dee36/pages/about.md) page in your new repository will be the landing page for the How-to Guide.

1. Add general information about the guide you are creating to the `About` section.
2. Add citation instructions to the `Please cite this guide as follows` section.
3. Add acknowledgments and references to the `Acknowledgements` and `References` sections, respectively. 
4. Update the title for this page. This update should be made in the markdown header. See example code below.

```yaml
---
title: How-to Guide for creating a How-to Guide
toc: false
---
```

The `toc: false` indicates that a floating table of contents will NOT be included for the headings on the `About` page.


## 8. Deploy to GitHub pages

To deploy your guide to GitHub pages:

1. Go to your repository `Settings`;
2. Select `Pages` from the left hand navigation menu;
3. In the `Source` drop-down menu select `Deploy from branch`;
4. In the `Branch` drop-down menu select `Main`; and,
5. Click `Save`

The documentation for GitHub provides additional information on how to [**set up GitHub pages for your repository**](https://pages.github.com/). Make sure to select the options `Project site` and `Start from scratch`: this will provide a straightforward walkthrough for setting up GitHub pages.


### Deploy using GitHub actions

GitHub actions can also be used to deploy content using the ELIXIR Toolkit Theme (ETT). This is also required for more advanced configurations (e.g. including citations that are linked to a Zotero library).

Visit the documentation to [read more about GitHub actions](https://elixir-belgium.github.io/elixir-toolkit-theme/getting_started).


## 9. Testing functional content

As an example, some How-to Guides detail the use of the bioinformatics platform Galaxy and demonstrate its application to analysis of real world data. It is critical that the functional content included (tools, workflows, code) is tested by:

- The original developer ( *if this isn't you* ); and 
- New users who have never seen the content before

A good example is a bioinformatics workflow: this workflow should be tested to ensure it functions as expected. This makes it more likely that someone will be able to successfully reuse the part of the guide that refers to the workflow.


### Make sure that others can understand your How-to Guide
 
The How-to Guide you create will be more reusable if multiple people have worked through the content. They will either successfully complete the activities in the guide, or provide critical feedback that can be used to improve the How-to Guide.


### Add links that import a workflow to Galaxy

You can embed links into a How-to Guide that instruct a Galaxy instance to import a specific version of a workflow from a source like [Dockstore](https://dockstore.org/) or [WorkflowHub](https://workflowhub.eu/). The example use case is if you would like a user of your guide to be able to open a workflow by simply clicking a link.


#### Requirements for workflow import to Galaxy using an embedded link

1. Create a GitHub repository for your workflow - the guide [available here](https://australianbiocommons.github.io/how-to-doc-guidelines) describes how to use the BioCommons documentation guidelines template for this purpose
2. Commit your workflow to GitHub
3. Register the workflow with [WorkflowHub](https://workflowhub.eu/) - see the [getting started documentation for WorkflowHub](https://about.workflowhub.eu/docs/)
4. Build the required link, as described in the example below


#### Example 

An example workflow import link is included here for Galaxy Australia and WorkflowHub:

```
https://usegalaxy.org.au/workflows/trs_import?trs_server=workflowhub.eu&trs_id=221&trs_version=3
```

Breaking the link down into its components:

1. `https://usegalaxy.org.au/workflows/trs_import`: [Galaxy Australia](https://usegalaxy.org.au/), please initiate a workflow import using my account
2. `?trs_server=workflowhub.eu`: use the [WorkflowHub TRS](https://about.workflowhub.eu/developer/trs/) server, and
3. `&trs_id=221&trs_version=3`: import workflow ID `221`, version number `3`
4. Note that you can leave out the version, in which case Galaxy will provide the option to select a workflow version for import

{% include callout.html type="important" content="A user needs to log in to Galaxy first for the workflow import to be successful." %}

If you add these links, don't forget to also cite the workflow. Example for the workflow used above:
> Price, G., & Farquharson, K. (2022). PacBio HiFi genome assembly using hifiasm v2.1. WorkflowHub. https://doi.org/10.48546/WORKFLOWHUB.WORKFLOW.221.3


## 10. GitHub & Zenodo

1. [Create a GitHub release](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)
2. Link your repository to Zenodo. More information is [available in GitHub docs](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content). 


## 11. Adding the DOI to your guide

1. Update the DOI field in the `CITATION.cff` file: [example here](https://github.com/AustralianBioCommons/guide-template/blob/ef31713ddb011e3fed11ad36aacd993761f9d771/CITATION.cff) 

{% include callout.html type="note" content="Updating your `CITATION.cff` file allows GitHub to generate a citation for your repository automatically, which can be accessed in the repository 'About' menu." %}

{:start="2"}
2. Add the DOI (or even a complete citation!) into your how-to cite instructions on the `index.md` page. See example below:

```
Gustafsson, J., Al Bkhetan, Z., Shadbolt, M., Murigneux, V., Williams, S., 
Capon, P., Khan, F. Z., & Nelson, T. (2023). How-to Guide for creating a 
How-to Guide (Version 1.0.0) [Computer software]. https://doi.org/10.5281/zenodo.8210269
```

{% include callout.html type="important" content="A blank `CITATION.cff` example is provided below. Don't forget to fill out the other metadata in this file!" %} 

```yaml
cff-version: 0.0.0
message: "Please cite as below."
authors:
  - family-names: [family name goes here]
    given-names: [given names go here]
    orcid: [ORCID goes here]
title: "Title of repository goes here"
version: 0.0.0
doi: [DOI goes here]
date-released: YYYY-MM-DD
```


## 12. Now share the How-to Guide!
