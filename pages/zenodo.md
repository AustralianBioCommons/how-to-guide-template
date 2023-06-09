---
title: Creating GitHub releases and Zenodo DOIs
type: guides
contributors: [Johan Gustafsson]
description: How to create GitHub releases for your How-to Guide and link this to Zenodo to generate digital object identifiers (DOIs).
affiliations: [Australian BioCommons]
toc: false
---


## GitHub & Zenodo

1. [Create a GitHub release](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)
2. Link your repository to Zenodo. More information is [available in GitHub docs](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content). 


## Adding the DOI to your guide

{:start="3"}
3. Add the DOI (or even a complete citation!) into your how-to-cite instructions on the `index.md` page
4. Update the DOI field in the [`CITATION.cff` file](https://github.com/AustralianBioCommons/guide-template/blob/ef31713ddb011e3fed11ad36aacd993761f9d771/CITATION.cff) 

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
