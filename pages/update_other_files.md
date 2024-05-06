---
title: Update other required files
type: guides
description: How to update the content of other files required for your How-to Guide.
---


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
