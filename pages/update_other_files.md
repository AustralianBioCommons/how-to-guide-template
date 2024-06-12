---
title: Acknowledge contributions
type: guides
description: How to update the content of other files required for your How-to Guide.
---


## Updating `CONTRIBUTORS.yml`

Every time you add a contributor, you need to update the `CONTRIBUTORS.yml` file, which can be found in the `/data` directory.

This ensures that the added contributor:

1. Has their name included on each guide page where it has been added to the yaml header, and
2. Is provided with a tile in the Contributors section on the `about.md` page

The text you add to `CONTRIBUTORS.yml should be in this format:

```yaml
Firstname Lastname:
    git: github_username
    orcid: 0000-1234-5678-9012
    role: users_role
    affiliation: declared affiliation (not linked)
```


## Updating `affiliations.yml`

Every time you add a new affiliation, you need to update `affiliations.yml`, which can be found in the `/_data` directory. 

If you use affiliations in the yaml header content of any page, this will require this specific affiliation information to be available. 

A new example affiliation is available below: note that it also includes an image / logo which should be added to the `/images` directory.

```yaml
- name: Galaxy Australia
  image_url: /images/infrastructures/galaxy-aust-logo-portrait-CMYK.png
  expose: true
  type: infrastructure
  url: https://usegalaxy.org.au/
```

{% include callout.html type="note" content="You can add logos to the `/images` directory." %}
