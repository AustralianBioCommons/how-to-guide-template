---
title: Adding extras to improve your How-to Guide
description: How to add and configure elements from the ELIXIR Toolkit theme that will improve the appearance and function of your How-to Guides.
toc: true
---


## Updating the main configuration file: `_config.yml`

{% include callout.html type="important" content="You will only need to modify the `_config.yml` if you wish to make major changes to the way your new guide repository makes use of the remote ELIXIR ToolKit theme. Instructions for how to do this, and what the different options are, can be [found here](https://elixir-belgium.github.io/elixir-toolkit-theme/configuring_theme). " %}


## Navigation tiles

See the [ELIXIR Toolkit theme](https://elixir-belgium.github.io/elixir-toolkit-theme/overview_tiles#section-tiles-with-information) for more information.


### Include navigation tiles for all pages

To add tiles for guide pages that you have created, add the following code to the page you would like the tiles to appear on:

{% raw %}
```
{% include section-navigation-tiles.html type="guides" %}
```
{% endraw %}

{% include section-navigation-tiles.html type="guides" %}

### You can also add the following:

- `type="type_value"` : only shows tiles for pages that have the indicated `type_value` in the page header
- `search=true` : enables searching - useful for large tile sets
- `except="index.md"` : removes specific tiles


### Example - only pages of type `"type_value"`

{% raw %}
```
{% include section-navigation-tiles.html type="quick_start" %}
```
{% endraw %}

{% include section-navigation-tiles.html type="quick_start" %}


### Example - only pages of type `"guides"`

{% raw %}
```
{% include section-navigation-tiles.html type="guides" %}
```
{% endraw %}

{% include section-navigation-tiles.html type="guides" %}
