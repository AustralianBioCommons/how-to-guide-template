---
title: Adding new pages to your project
type: guides
contributors: [Johan Gustafsson]
description: How to create and update new pages for your How-to Guide.
affiliations: [Australian BioCommons]
toc: false
---


Individual pages are created using the [`guide_template.md`](docs/guide_template.md): use the template to create as many pages as you need for your guide (i.e. copy and rename the `guide_template.md` to create a new page).

## For each new page

1. Copy `guide_template.md` and rename it
2. Add these files to the `/docs` directory to keep your work organised
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
4. You can also add another optional line for `type`. This can be used to identify subsets of guide pages: for example if you want to include navigation tiles for only specific pages. An example is provided below.

```
type: guides
```

## Other required information

{:start="4"}
4. Add your name to `CONTRIBUTORS.yml`

This ensures your name renders properly on each guide page that it has been added to. 

The file can be found in the `/_data` directory.

{:start="5"}
5.  Update `affiliations.yml` (if needed)

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