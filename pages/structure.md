---
title: How to make sure your How-to Guide is configured properly
type: guides
contributors: [Johan Gustafsson]
description: How to modify the template configuration files to make sure your How-to Guide web pages function as expected.
affiliations: [Australian BioCommons]
toc: false
---


The `_config.yml` and `main.yml` (located in `_data/sidebars/`) files determine the structure of your web pages and which items appear in the navigation menu on the left hand side, respectively.

{% include callout.html type="important" content="You will only need to modify the `_config.yml` if you wish to make major changes to the way the template repository makes use of the remote ELIXIR ToolKit theme. Instructions for how to do this, and what the different options are, can be [found here](https://elixir-belgium.github.io/elixir-toolkit-theme/configuring_theme). " %}

Each new page that is included needs to be added to the `main.yml` file so that it appears in the left hand navigation menu. An example of this code is provided below for the current How-to Guide:

```

```