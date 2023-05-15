---
title: Adding new pages to your project
type: guides
contributors: [Johan Gustafsson]
description: How to create and update new pages for your How-to Guide.
affiliations: [Australian BioCommons]
---


Individual pages are created using the [`example_page.md`](https://github.com/AustralianBioCommons/guide-template/blob/ef31713ddb011e3fed11ad36aacd993761f9d771/pages/example_page.md): use the template to create as many pages as you need for your guide (i.e. copy and rename the `example_page.md` to create a new page).

## For each new page

1. Copy contents of `example_page.md` into a new file and rename it
2. Add these files to the `/pages` directory to keep your work organised
3. Update the header content. An example of this is included below. You need to add a `title`, `contributors`, `description` and `affiliations`.

```
---
title: [How-to Guide template]
contributors: [Johan Gustafsson]
description: Add a plain text description here.
affiliations: [Australian BioCommons]
---   
```

{:start="4"}
4. You can also add another optional line for `type`. Example code is provided below. This can be used to identify subsets of guide pages: for example if you want to include navigation tiles for only specific pages (see [Optional extra features](extras.md)). This text will also appear at the top of the page in the final website: [an example is available here](https://australianbiocommons.github.io/how-to-guide-template/add_new_pages). 

```
type: guides
```

## Adding new pages to your guide configuration files

{:start="5"}
5. Each new page that is included needs to be added to the `main.yml` file so that it appears in the left hand navigation menu. An example of this code is provided below for the current How-to Guide:

```
subitems:
  - title: About
    url: /
  - title: 1. Create a new repository
    url: /create_new
  - title: 2. Update your landing page content
    url: /update_index
  - title: 3. Add new pages to your guide
    url: /add_new_pages
  - title: 4. Update configuration files
    url: /structure
  - title: 5. Test and improve your guide content
    url: /improve_content
  - title: 6. Make your guide citable
    url: /zenodo
  - title: Optional extra features
    url: /extras
  - title: Contributors
    url: /contributors
```

There are many other options for configuring your guide web page differently and adding more complicated page and navigation structures. For more information please visit the [ELIXIR Toolkit theme documentation](https://elixir-belgium.github.io/elixir-toolkit-theme/).

{% include callout.html type="important" content="You will only need to modify the `_config.yml` if you wish to make major changes to the way your new guide repository makes use of the remote ELIXIR ToolKit theme. Instructions for how to do this, and what the different options are, can be [found here](https://elixir-belgium.github.io/elixir-toolkit-theme/configuring_theme). " %}


## Images & message boxes

Including images and message boxes can make your guide much easier to read and understand. Some examples of how to add these elements to your guide are included below.

More details on images and message boxes can be found in the [documentation for the ELIXIR Toolkit theme](https://elixir-belgium.github.io/elixir-toolkit-theme/markdown_cheat_sheet#message-boxes).


### Image

The two options for including images are shown below, and an example of the second option is shown rendered on this page.

{% raw %}
```
![](./images/main_logo.png)
{% include image.html file="/images/main_logo.png" caption="Figure 1. The Australian BioCommons logo." alt="Australian BioCommons logo" max-width="10" %}
```
{% endraw %}

{% include image.html file="/images/main_logo.png" caption="Figure 1. The Australian BioCommons logo." alt="Australian BioCommons logo" max-width="10" %}


### Message boxes

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


## Contributors and affiliations

{:start="6"}
6. Add your name to [`CONTRIBUTORS.yml`](https://github.com/AustralianBioCommons/guide-template/blob/ef31713ddb011e3fed11ad36aacd993761f9d771/_data/CONTRIBUTORS.yml)

This ensures your name renders properly on each guide page that it has been added to. 

The file can be found in the `/_data` directory.

{:start="7"}
7. Update [`affiliations.yml`](https://github.com/AustralianBioCommons/guide-template/blob/ef31713ddb011e3fed11ad36aacd993761f9d771/_data/affiliations.yml) (if needed)

If you are adding a new affiliation, also update `affiliations.yml`, which can also be found in the `/_data` directory. 
   - The affiliations in the header content above require this information to be available. 
   - A new example affiliation is available below: note that it also includes an image / logo which should be added to the `/images` directory.

```
- name: Galaxy Australia
  image_url: /images/infrastructures/galaxy-aust-logo-portrait-CMYK.png
  expose: true
  type: infrastructure
  url: https://usegalaxy.org.au/
```

{% include callout.html type="note" content="You can add logos to the `/images` directory." %}