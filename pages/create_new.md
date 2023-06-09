---
title: Creating a new How-to Guide repository
type: guides
contributors: [Johan Gustafsson]
description: How to create and begin updating a repository for your new How-to Guide, based on a template repository.
affiliations: [Australian BioCommons]
toc: false
---


1. Create a new repository

{% include callout.html type="important" content="Use [**this template repository**](https://github.com/AustralianBioCommons/guide-template) to create a new repository in your GitHub account or organisation." %}

2. Understand its structure

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