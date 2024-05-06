---
title: A multi-page How-to Guide
type: option
description: How to create and update new pages for your How-to Guide.
toc_depth: 2
---


## Updating the main How-to Guide page: index.md

For a single page guide, the `index.md` page will usually contain the entire How-to Guide. However, the role of this page changes for a multi-page guide.

The most straightforward use for the `index.md` page in this case is as a `Quick start guide` or `Landing page` where a reader is provided with introductory content to help them understand and navigate the How-to Guide you have written. 

The guide you are currently reading is a good example of this structure:

The first part of the `index.md` provides some introductory information:

```
This guide describes *How-to* create new How-to Guide websites using a GitHub repository template. 

**What are How-to Guides?** They are step-by-step guides that support the reuse of bioinformatics tools, workflows and data on Australian compute systems and infrastructure.

The template described in these docs aims to:
- **Reduce the time you spend** creating guides by providing a standard structure to develop and maintain guidance material;
- **Provide further guide templates** for common use cases of the How-to Guides concept;
- Allow you to **easily deploy these guides** using GitHub pages and a remote theme provided by ELIXIR; and,
- Allow linking to Zenodo and **creation of DOIs** for each release. You created the content, others should be able to cite it!

{% include callout.html type="note" content="the instructions below are for a simple guide that can accommodate a few pages only: if you require more complicated structures, please contact @supernord via GitHub" %}
```

The second part of the `index.md` provides a quick start description, with links to the relevant pages:

```
These are the steps required to make use of the contents of the How-to Guide template repository:

1. [Fork the template repository](https://github.com/AustralianBioCommons/guide-template) - see [this page](create_new) for more details
2. [A single or multi-page guide?](select_type)
3. [Add a single new page to your guide](add_single_page)
4. Optional: [Adding multiple new pages to your guide](add_new_pages)
5. [Update your About page content](update_about)
6. [Test, review and improve your guide content](improve_content)
7. [When ready create a GitHub release and link to Zenodo to create a DOI](zenodo)

Then share the How-to Guide!
```


## Add new page


### Add new page

1. Copy contents of `example_page.md` into a new file and rename it
2. Add these files to the `/pages` directory to keep your work organised
3. Update the header content. An example of this is included below. You need to add a `title`, `contributors`, `description` and `affiliations`

```yaml
---
title: [How-to Guide template]
contributors: [Johan Gustafsson]
description: Add a plain text description here.
affiliations: [Australian BioCommons]
---   
```

{:start="4"}
4. You can also add another optional line for `type`. 
   - Example code is provided below. 
   - This can be used to identify subsets of guide pages: for example if you want to include navigation tiles for only specific pages (see [Optional extra features](extras.md)). 
   - This text will also appear at the top of the page in the final website: [an example is available here](https://australianbiocommons.github.io/how-to-guide-template/add_new_pages). 

```yaml
type: guides
```


### Update navigation bar

{:start="5"}
5. Each new page that is included needs to be added to the `main.yml` file so that it appears in the left hand navigation menu. Below is the `main.yml` from the template repository:
```yaml
subitems:
  - title: Home
    url: /index
  - title: Example page
    url: /example_page
  - title: Contributors
    url: /contributors
```

To create the guide you are currently viewing, this code was updated as follows:

```yaml
subitems:
  - title: Quick start
    url: /
  - title: 1. Create a new repository
    url: /create_new
  - title: 2. A single or multi-page guide?
    url: /select_type
  - title: 3. Add a single new page to your guide
    url: /add_single_page
  - title: 4. Adding multiple new pages to your guide
    url: /add_new_pages
  - title: 5. Update your About page content
    url: /update_about
  - title: 6. Test & improve your guide content
    url: /improve_content
  - title: 7. Make your guide citable
    url: /zenodo
  - title: Adding optional features
    url: /extras
  - title: Usage examples
    url: /examples
```

Note a few things:
- The landing page url can be either `/index` or `/`
- You can specify the order and structure of the navigation bar in `main.yml`
- You can also add a title element and a link: this is shown below, with the `title_url` set to the landing page `index.md` for the guide

```yaml
title: Navigation bar title
title_url: /
subitems:
  - title: Home
    url: /index
  - title: Example page
    url: /example_page
  - title: Contributors
    url: /contributors
```

There are many other options for configuring your guide web page differently and adding more complicated page and navigation structures. For more information please visit the [ELIXIR Toolkit theme documentation](https://elixir-belgium.github.io/elixir-toolkit-theme/).
