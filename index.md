---
title: Creating a How-to Guide
sidebar: false
toc_depth: 2
---

This guide describes *How-to* create new How-to Guide websites using a GitHub repository template. 

**What are How-to Guides?** They are step-by-step guides that support the reuse of bioinformatics tools, workflows and data on Australian compute systems and infrastructure.

The template described in these docs aims to:
- **Reduce the time you spend** creating guides by providing a standard structure to develop and maintain guidance material;
- **Provide further guide templates** for common use cases of the How-to Guides concept;
- Allow you to **easily deploy these guides** using GitHub pages and a remote theme provided by ELIXIR; and,
- Allow linking to Zenodo and **creation of DOIs** for each release. You created the content, others should be able to cite it!

{% include callout.html type="note" content="the instructions below are for a simple guide that can accommodate a few pages only: if you require more complicated structures, please contact @supernord via GitHub" %}


These are the steps required to make use of the contents of the How-to Guide template repository:

2. [A single or multi-page guide?](select_type)
3. [Add a single new page to your guide](add_single_page)
4. Optional: [Adding multiple new pages to your guide](add_new_pages)
5. [Acknowledge contributions](update_other_files)
6. [Update your About page content](update_about)
7. [Deploy to GitHub pages](deploy)
8. [Test, review and improve your guide content](improve_content)
9. [When ready create a GitHub release and link to Zenodo to create a DOI](zenodo)

Then share the How-to Guide!


## 1. Fork the template repository

1. Fork [**the template repository available at this link**](https://github.com/AustralianBioCommons/guide-template) to create a new repository in your GitHub account or organisation.


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

