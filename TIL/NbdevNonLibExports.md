---
title: "NBDev Non Lib Exports"
author: "Isaac Flath"
date: "2024-9-21"
description: "Nbdev export of notebooks that aren't libraries"
categories: [FastHTML, Python, Web Development, Nbdev]
---

# Today I Learned

`nbdev` has a single notebook export command that allows you to export notebooks without them being treated as a library.

This is done with the command `nb_export`.

In order to apply this to a directory and export them to an app for building FastHTML apps in notbooks, the command is `find nbs -name "*.ipynb" -print0 | xargs -0 -I {} nb_export --lib_path app {}`