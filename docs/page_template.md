---
layout: default
title: Template
---
# Feature Name or Use Case Name **[TIER]** (1)
<!--If writing about a use case, drop the tier, and start with a verb,
for example, "Configure", "Implement", + the goal/scenario-->

<!--For pages on newly-introduced features, add the following line.
If only some aspects of the feature have been introduced, specify which parts of the feature.-->
> [Introduced](link_to_issue_or_mr) in GitLab (Tier) X.Y (2).

An introduction -- without its own additional header -- goes here.
Offer a description of the feature or use case, and what to expect on this page.
(You can reuse this content, or part of it, for the front matter's `description` at the top
of this file).

The introduction should answer the following questions:

- What is this feature or use case?
- Who is it for?
- What is the context in which it is used and are there any prerequisites/requirements?
- What can the audience do with this? (Be sure to consider all applicable audiences, like
  GitLab admin and developer-user.)
- What are the benefits to using this over any alternatives?

## Use cases

Describe some use cases, typically in bulleted form. Include real-life examples for each.

If the page itself is dedicated to a use case, this section can usually include more specific
scenarios for use (for example, variations on the main use case), but if that's not applicable,
the section can be omitted.

Examples of use cases on feature pages:
- CE and EE: [Issues](../../user/project/issues/index.md#use-cases)
- CE and EE: [Merge Requests](../../user/project/merge_requests/index.md)
- EE-only: [Geo](../../administration/geo/replication/index.md)
- EE-only: [Jenkins integration](../../integration/jenkins.md)

## Requirements

State any requirements for using the feature and/or following along with the instructions.

These can include both:
- technical requirements (for example, an account on a third party service, an amount of storage space,
  prior configuration of another feature)
- prerequisite knowledge (for example, familiarity with certain GitLab features, cloud technologies)

Link each one to an appropriate place for more information.

## Instructions

This is the part of the document where you can include one or more sets of instructions.
Each topic should help users accomplish a specific task.

Headers should describe the task the reader will achieve by following the instructions within,
typically starting with a verb. For example, `Create a package` or `Configure a pipeline`.

Larger instruction sets may have subsections covering specific phases of the process.
Where appropriate, provide examples of code or configuration files to better clarify
intended usage.

- Write a step-by-step guide, with no gaps between the steps.
- Include example code or configurations as part of the relevant step.
  Use appropriate Markdown to wrap code blocks with
  [syntax highlighting](../../user/markdown.md#colored-code-and-syntax-highlighting).
- Start with an h2 (`##`), break complex steps into small steps using
  subheadings h3 > h4 > h5 > h6. _Never skip a hierarchy level, such
  as h2 > h4_, as it will break the TOC and may affect the breadcrumbs.
- Use short and descriptive headings (up to ~50 chars). You can use one
  single heading like `## Configure X` for instructions when the feature
  is simple and the document is short.

Example topic:

## Create a teddy bear

Start by writing a sentence or two about _why_ someone would want to perform this task.
It's not always possible, but is a good practice. For example:

Create a teddy bear when you need something to hug.

Follow this information with the task steps.

To create a teddy bear:

1. Go to **Settings > CI/CD**.
1. Expand **This** and click **This**.
1. Do another step.

After the numbered list, add a sentence with the expected result, if it
is not obvious, and any next steps. For example:

The teddy bear is now in the kitchen, in the cupboard above the sink.

You can retrieve the teddy bear and put it on the couch with the other animals.

Screenshots are not necessary. They are difficult to keep up-to-date and can clutter the page.

<!-- ## Troubleshooting

Include any troubleshooting steps that you can foresee. If you know beforehand what issues
one might have when setting this up, or when something is changed, or on upgrading, it's
important to describe those, too. Think of things that may go wrong and include them here.
This is important to minimize requests for support, and to avoid doc comments with
questions that you know someone might ask.

Each scenario can be a third-level heading, for example, `### Getting error message X`.
If you have none to add when creating a doc, leave this section in place
but commented out to help encourage others to add to it in the future. -->

---

Notes:

- (1): Apply the [tier badges](styleguide.md#product-badges) accordingly
- (2): Apply the correct format for the
       [GitLab version that introduces the feature](styleguide.md#gitlab-versions-and-tiers)
