---
layout: default
title: Use Pivotal Tracker commit commands
parent: Git
nav_order: 2
---

# Pivotal Tracker Updates in SCM Post-Commit Hooks

To associate an SCM commit with specific Tracker stories, Tracker looks for a special syntax in the commit message 
string to indicate one or more story IDs and (optionally) a state change for the story.
Your commit message should contain one pair of square brackets, containing one or more sets of a hash character followed
 immediately by a story ID.

## Syntax

The minimum commit message string that will allow Tracker to associate 
a commits POST with a story and create a comment is a single story ID enclosed in square brackets: '\[#12345678\]'. 
A more typical message, indicating that one commit completes two stories (which need not be in the same Tracker project), 
might look like this: 'finally \[finished #12345678 #12345779\], fixes client/server integration glitch'


If an included story was not already started (it was in the "not started" state), an update to that story 
that doesn't contain any other state-change information will automatically start the story.

To automatically finish a story by using a commit message, include "fixed", "completed", or "finished" in the square
brackets in addition to the story ID. You may use different cases or forms of these verbs, such as "Fix" or "FIXES",
and they may appear before or after the story ID.

**Of course it's best to always use the present tense in a commit message.**

## Notes

For features, use of one of these keywords will put the story 
in the finished state. For chores, it will put the story in the accepted state.

In some environments, code that is committed is automatically deployed. For this situation, use the keyword "delivers" 
and feature stories will be put in the delivered state.

## This document is based on 
[Pivotal Tracker Special Endpoint Usage - API Docs](https://www.pivotaltracker.com/help/api?version=v5#Tracker_Updates_in_SCM_Post_Commit_Hooks)

###### *Author: Roberto Cabassi Bombardieri*
