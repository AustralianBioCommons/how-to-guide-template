---
title: Creating GitHub releases and Zenodo DOIs
type: guides
description: How to create GitHub releases for your How-to Guide and link this to Zenodo to generate digital object identifiers (DOIs).
toc: false
---


## GitHub & Zenodo

1. [Create a GitHub release](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)
2. Link your repository to Zenodo. More information is [available in GitHub docs](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content). 


## Adding the DOI to your guide

{:start="3"}
3. Update the DOI field in the `CITATION.cff` file: [example here](https://github.com/AustralianBioCommons/guide-template/blob/ef31713ddb011e3fed11ad36aacd993761f9d771/CITATION.cff) 

{% include callout.html type="note" content="Updating your `CITATION.cff` file allows GitHub to generate a citation for your repository automatically, which can be accessed in the repository 'About' menu." %}

{:start="4"}
4. Add the DOI (or even a complete citation!) into your how-to cite instructions on the `index.md` page. See example below:

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
