---
layout: post
title: "pinax-theme-bootstrap 2.0.1.1 Release Notes"
date: 2012-03-09 03:53:02
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/p/pinax-theme-bootstrap/pinax-theme-bootstrap-2.0.1.1.tar.gz>

This release includes the following:

* bumped version to 2.0.1.1
* added conditional django-staticfiles install_requires requirement
* remove static files from install_requires for now. need to make this conditional django < 1.4
* use bootstrap modal
* move html5 shim below styles
* move scripts to the bottom of the page
* Remove hardcoded path and duplicate change from 2.0.2-wip by DominikTo
* added maxheight option for modals
* Corrected white icons asset url.
