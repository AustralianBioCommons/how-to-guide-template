---
title: Adding extras to improve your How-to Guide
contributors: [Johan Gustafsson]
description: How to add and configure elements from the ELIXIR Toolkit theme that will improve the appearance and function of your How-to Guides.
toc: true
---


## Navigation tiles

See the [ELIXIR Toolkit theme](https://elixir-belgium.github.io/elixir-toolkit-theme/overview_tiles#section-tiles-with-information) for more information.


### Include navigation tiles for all pages

To add tiles for guide pages that you have created, add the following code to the page you would like the tiles to appear on:

{% raw %}

{% include section-navigation-tiles.html type="guides" %}

{% endraw %}

{% include section-navigation-tiles.html type="guides" %}

You can also add the following:
- `type="type_value"` : only shows tiles for pages that have the indicated `type_value` in the page header
- `search=true` : enables searching - useful for large tile sets
- `except="index.md"` : removes specific tiles


### Example - only pages of type `"quick_start"`

{% raw %}

{% include section-navigation-tiles.html type="quick_start" %}

{% endraw %}

{% include section-navigation-tiles.html type="quick_start" %}


### Example - only pages of type `"template"`

{% raw %}

{% include section-navigation-tiles.html type="template" %}

{% endraw %}

{% include section-navigation-tiles.html type="template" %}


### Example - only pages of type `"guides"`

{% raw %}

{% include section-navigation-tiles.html type="guides" %}

{% endraw %}

{% include section-navigation-tiles.html type="guides" %}
