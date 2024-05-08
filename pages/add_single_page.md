---
title: A single page How-to Guide
type: option-1
description: How to create and update a How-to Guide with a single main content page.
toc_depth: 2
---


## What needs to be updated for a single page guide?

For a single page How-to Guide all of your content (i.e. the information or guidance you would like to share) should be added to `index.md`.


## Updating the main How-to Guide page: index.md

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


## Page templates

The template repository already contains some example structures that can be used for the content of `index.md`, and include:

- [Standard page that can be used as a starting point for any type of guide](https://australianbiocommons.github.io/guide-template/example_page)
- [Suggested structure for a guide describing how to use a bioinformatics workflow](https://australianbiocommons.github.io/guide-template/example_bioinformatics_workflow_page)
- [Suggested structure for documentation describing a workflow: based on Australian BioCommons documentation guidelines](https://australianbiocommons.github.io/guide-template/example_workflow_documentation_page)

To use any of these examples, simply copy the markdown content from the relevant example file into the `index.md` file in your repository.

{% include callout.html type="tip" content="You can also build custom markdown down content using tools like [readme.so](https://readme.so/)." %}

