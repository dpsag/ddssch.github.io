---
layout: default
title: How to setup Husky to automate testing, building, and linting
parent: Git
nav_order: 3
---

# How to setup Husky to automate testing, building, and linting

As more and more developers work on a project, it becomes more and more difficult to avoid CI errors, in particular when auto deploying projects from develop to staging

## What the want to accomplish

- Avoid the CI pipeline to fail

### Install husky and pretty-quick

Husky v4 and above still has some issues regarding the auto discovery of node, in particular when using a GUI git client. Many developers suggest to stick with version 3.x

At first, after the script section of the package.json, let's put the configuration needed for Husky:

```
"husky": {
    "hooks": {
      "pre-commit": "echo 'Running prettier before committing'; pretty-quick --staged",
      "pre-push": "echo 'Running tests for project buildability'; quasar build"
    }
  },
```

Then we can install husky and pretty-quick (the latter to auto commit prettified files)

```npm i --save-dev husky@3 pretty-quick```

### Tips

You can run ```npm rebuild``` to reinstall git commit hooks if for any reason the installation failed.

###### *Author: Roberto Cabassi Bombardieri*
