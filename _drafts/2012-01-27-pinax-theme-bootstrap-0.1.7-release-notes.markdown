---
layout: post
title: "pinax-theme-bootstrap 0.1.7 Release Notes"
date: 2012-01-27 09:05:42
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/p/pinax-theme-bootstrap/pinax-theme-bootstrap-0.1.7.tar.gz>

This release includes the following:

* update README
* update README
* Merge branch 'master' into 2.0-wip
* bump version
* remove outdated todo items
* update to latest bootstrap, new structure /  / we now ship unmodified bootstrap media, with / overrides happening in our theme.less file. / this make upgrades easier and keeps things / cleaner. also switched to using the static / templatetag for media.
* Use user_display
* update to latest css
* update to latest js sources
* 0.1.6
* Handle multi-part forms
* update to latest version
* switch to use proper alert classes
* fix account menu dropdown /  / Conflicts: /  / 	pinax_theme_bootstrap/templates/_account_bar.html
* change login and signup templates to 8-4 columns instead of 9-3
* fixed copy paste error in sign up sidebar include
* put sign up page into a span9 with a blank sidebar that can be overridden; factored out terms/privacy text to include
* put log in page into a span9 with a blank sidebar that can be overridden
* alphabetize javascript includes, add new ones
* adding some notes about upgrading from bootstrap 1.x
