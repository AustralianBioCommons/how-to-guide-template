---
title: A multi-page How-to Guide
type: option
description: How to create and update new pages for your How-to Guide.
toc_depth: 2
---


## Quick description of the process

1. [Update the `index.md` file](#updating-the-main-how-to-guide-page-indexmd)
2. [Create a new markdown file in the `/pages` directory](#for-each-new-page)
2. Give this file a unique name (e.g. `new-page-name.md`)
3. Add your content to this file
4. Option: use an existing template for the markdown content to make your life easier: see [page templates section](#page-templates)
5. 
6. Repeat steps #1-5 to create as many pages as you need for your guide


## Detailed guide

### Updating the main How-to Guide page: index.md

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


### Page templates

The template repository already contains some example structures that can be used for the content of your guide pages, and include:

- [Standard page that can be used as a starting point for any type of guide](https://australianbiocommons.github.io/guide-template/example_page)
- [Suggested structure for a guide describing how to use a bioinformatics workflow](https://australianbiocommons.github.io/guide-template/example_bioinformatics_workflow_page)
- [Suggested structure for documentation describing a workflow: based on Australian BioCommons documentation guidelines](https://australianbiocommons.github.io/guide-template/example_workflow_documentation_page)

To use any of these examples, simply copy the markdown content from the relevant example file into the `index.md` file in your repository.

{% include callout.html type="tip" content="You can also build custom markdown down content using tools like [readme.so](https://readme.so/)." %}


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

{% include callout.html type="important" content="You will only need to modify the `_config.yml` if you wish to make major changes to the way your new guide repository makes use of the remote ELIXIR ToolKit theme. Instructions for how to do this, and what the different options are, can be [found here](https://elixir-belgium.github.io/elixir-toolkit-theme/configuring_theme). " %}

{:start="6"}
6. Add your name to [`CONTRIBUTORS.yml`](https://github.com/AustralianBioCommons/guide-template/blob/ef31713ddb011e3fed11ad36aacd993761f9d771/_data/CONTRIBUTORS.yml)
   - This ensures your name renders properly on each guide page that it has been added to. 
   - The file can be found in the `/_data` directory.

The text you add should look like this:

```yaml
Firstname Lastname:
    git: github_username
    email: users@email.com
    orcid: 0000-1234-5678-9012
    role: users_role
    affiliation: declared affiliation (not linked)
```

Once a user is listed in this way in this file, a tile will be generated on the Contributors page.

{:start="7"}
7. If you added an affiliation above, update [`affiliations.yml`](https://github.com/AustralianBioCommons/guide-template/blob/ef31713ddb011e3fed11ad36aacd993761f9d771/_data/affiliations.yml)

8. If you are adding a new affiliation, also update `affiliations.yml`, which can also be found in the `/_data` directory. 
   - The affiliations in the header content above require this information to be available. 
   - A new example affiliation is available below: note that it also includes an image / logo which should be added to the `/images` directory.

```yaml
- name: Galaxy Australia
  image_url: /images/infrastructures/galaxy-aust-logo-portrait-CMYK.png
  expose: true
  type: infrastructure
  url: https://usegalaxy.org.au/
```

{% include callout.html type="note" content="You can add logos to the `/images` directory." %}


### Adding images & message boxes

Including images and message boxes can make your guide much easier to read and understand. Some examples of how to add these elements to your guide are included below.

More details on images and message boxes can be found in the [documentation for the ELIXIR Toolkit theme](https://elixir-belgium.github.io/elixir-toolkit-theme/markdown_cheat_sheet#message-boxes).


#### Images

The two options for including images are shown below, and an example of the second option is shown rendered on this page.

{% raw %}
```
![](./images/main_logo.png)
{% include image.html file="/main_logo.png" caption="Figure 1. The Australian BioCommons logo." alt="Australian BioCommons logo" max-width="10" %}
```
{% endraw %}

{% include image.html file="/main_logo.png" caption="Figure 1. The Australian BioCommons logo." alt="Australian BioCommons logo" max-width="10" %}


#### Message boxes

Four types of message boxes can also be included on your page: 
- `note`
- `tip`
- `important`, and
- `warning`

These are incredibly useful for emphasising important points in your guide.
An example is provided below, showing first the raw code you need to use and then an example warning message box.

{% raw %}
```
{% include callout.html type="TYPE OF MESSAGE BOX TEXT GOES HERE" content="THE CONTENT FOR YOUR MESSAGE BOX GOES HERE" %}
{% include callout.html type="warning" content="Definitely pay attention to this message box!" %}
```
{% endraw %}

{% include callout.html type="warning" content="Definitely pay attention to this message box!" %}


