---
layout: default
title: How to write a proper commit message
parent: Git
nav_order: 1
---

# How to write a proper commit message

Many developers write many different things.
 
This document explains how to write a good commit message.

## What the want to accomplish

- Ease of readability by other developers
- Automatic changelog creation based on git history, if needed
- Simple navigation trough git history when searching for a specific change

## The commit message

### Rules for a great commit message

- Separate subject from body with a blank line
- Limit the subject line to 70 characters
- Capitalize the subject
- Do not end the subject line with a period
- Use the imperative mood in the subject line
- Wrap the body at 80 characters
- Use the body to explain what and why vs. how

### Format the commit message

```
<type>(<scope?>): <subject> #tracker-id

<body?>

<footer?>
```

### Some examples

```
fix(ui): Ensure Range headers adhere more closely to RFC 2616 #2310

Add one new dependency, use `range-parser` (Express dependency) to compute
the range.
It is more well-tested in the wild.

BREAKING CHANGE:
port-runner command line option has changed to runner-port.
To migrate your project, change all the commands,
where you use --port-runner to --runner-port.
```

### Message subject (first line)

The first line cannot be longer than 70 characters, the second line is always blank.
The type and scope should always be lowercase as shown below.

#### Allowed <type> values:

- **feat** - new feature for the user, not a new feature for build script
- **fix** - bug fix for the user, not a fix to a build script
- **docs** - changes to the documentation
- **style** - formatting, missing semi colons, etc; no production code change
- **refactor** - refactoring production code, eg. renaming a variable
- **impr** - improve a current implementation without adding a new feature or fixing a bug.
- **test** - adding missing tests, refactoring tests; no production code change
- **chore** - updating grunt tasks etc; no production code change
- **perf** - change that improves performance
- **revert** - reverts a previous commit
- **build** - changes that affect the build system or external dependencies (example scopes: gulp, npm, Xcode, Android Studio)
- **ci** - changes to our Continuous Integrations configuration files and scripts (example scopes: Travis, Circle CI, Azure DevOps)

#### Example <scope> values:

- ui, api, VueComponentName, etc...

**TIP**
{: .label .label-green }

The `<scope>` can contain more values separated by a comma. Example: fix(ui,cli): Cordova mode added.

The `<scope>` can be empty (e.g. if the change is a global), in which case the parentheses are omitted.

## Message body

- uses the imperative, present tense: “change” not “changed” nor “changes”
- includes motivation for the change and contrasts with previous behavior

You must insert a message body only for public repos, for public apis and in general in projects with a certain amount of complexity.

You may insert a message body when the message subject is not self-explanatory.


## This document is based on 
[AngularJS Git Commit Msg Convention](https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit#)

###### *Author: Roberto Cabassi Bombardieri*
