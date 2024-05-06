---
title: A single page How-to Guide
type: option
description: How to create and update a How-to Guide with a single main content page.
toc_depth: 2
---


## What needs to be updated for a single page guide?

**For a single page How-to Guide all of your content (i.e. the information or guidance you would like to share) should be added to [index.md](https://github.com/AustralianBioCommons/guide-template/blob/132851cbc0bb112cafbaa623487e4524af5dee36/index.md).**


## Updating the main How-to Guide page: index.md

1. Select the markdown structure you would like to add to your How-to Guide
2. Open `index.md`
3. Copy the selected content into `index.md`
4. Update the yaml header content. An example of this is included below. 
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

{:start="4"}
4. If you have added contributors or affiliations you need to update [additional files](update_other_files)
5. You can also add another optional line for `type`. 
   - Example code is provided below. 
   - This can be used to identify subsets of guide pages: for example if you want to include navigation tiles for only specific pages (see [Optional extra features](extras.md)). 
   - This text will also appear at the top of the page in the final website: [an example is available here](https://australianbiocommons.github.io/how-to-guide-template/add_new_pages). 

```yaml
type: guides
```
4. Proceed to the next step: [adding content to the About page](update_about)

{% include callout.html type="tip" content="You can also build custom markdown down content using tools like [readme.so](https://readme.so/)." %}

The template repository already contains some example structures that can be used for the content of `index.md`, and include:

- [Standard page that can be used as a starting point for any type of guide](https://australianbiocommons.github.io/guide-template/example_page)
- [Suggested structure for a guide describing how to use a bioinformatics workflow](https://australianbiocommons.github.io/guide-template/example_bioinformatics_workflow_page)
- [Suggested structure for documentation describing a workflow: based on Australian BioCommons documentation guidelines](https://australianbiocommons.github.io/guide-template/example_workflow_documentation_page)

To use any of these examples, simply copy the markdown content from the relevant example file into the `index.md` file in your repository.



