---
layout: post
title: "pinax-theme-bootstrap 2.0.3 Release Notes"
date: 2012-05-21 23:14:32
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/p/pinax-theme-bootstrap/pinax-theme-bootstrap-2.0.3.tar.gz>

This release includes the following:

* version 2.0.3
* update to jquery 1.7.2
* remove old less.js
* update bootstrap media to 2.0.3
* Remove extra quote /  / Signed-off-by: Simon Luijk <simon@simonluijk.com>
* New url library drops support for the comma syntax for separating arguments /  / Signed-off-by: Simon Luijk <simon@simonluijk.com>
* require django-forms-bootstrap
* remove forms handling, point to django-forms-bootstrap
* Merge branch 'move-to-subdir' /  / * move-to-subdir: /   Add BC shims /   Make sure to extend the correct file /   Update docs /   Move all of the theme specific stuff into a subdirectory /  / Conflicts: / 	pinax_theme_bootstrap/templates/theme_base.html
* Add BC shims
* Make sure to extend the correct file
* Update docs
* Move all of the theme specific stuff into a subdirectory
* Changed url tags to django 1.4 style /  / Using doublequotes (") to follow coding conventions of the project
* add block for overriding of user dropdown links
* only show "logged in as" label if user is logged in
* use pipe as title delimiter
* removing unnecessary field set on forms and i18n on buttons
* use proper header in all templates, plus some other i18n and form changes that snuck in
* "logged in as" label and i18n account bar
* add section to readme about disabling responsive
* update form example
