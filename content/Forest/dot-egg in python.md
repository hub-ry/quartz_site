---
tags:
  - Forest
---


.egg-info is a directory created by Python's packaging system when you install a package in editable mode (pip install -e .). It contains metadata about your package.


### What's inside .egg-info?

- PKG-INFO - Package name, version, description, authors

- SOURCES.txt - List of all source files in your package

- requires.txt - Dependencies your package needs

- top_level.txt - Top-level module names

- dependency_links.txt - Links to dependencies (usually empty)




## Why it gets created

When you run pip install -e .:

1. Python reads your pyproject.toml

2. It installs your package in "editable" mode (changes to source code take effect immediately)

3. It creates .egg-info to track what was installed





It is commonly added to a .gitignore becuase 

1. It is  a build artifact
2. It's environment-specific
3. It's regenerated automatically
4. Clutters repo





Analogy to simplify: 

If your source code is a recipe, the .egg-info is a shopping list generated from the recipe (don't commit this)



## Best practice

Standard Python practice is to ignore:

- .egg-info/ directories

- .egg files

- build/ and dist/ directories

- __pycache__/ directories

These are all generated files that can be recreated from your source code.