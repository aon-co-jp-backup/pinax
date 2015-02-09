---
layout: post
title: "pinax-theme-bootstrap 5.7.0 Release Notes"
date: 2015-02-08 23:37:31
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/p/pinax-theme-bootstrap/pinax-theme-bootstrap-5.7.0.tar.gz>

This release includes the following:

* Add missing bootstrap.min.js file /  / Closes #85
* Correct path for bootstrap.min.js
* remove <br /> and tweak spacing with css
* provide cross links to signup and login (#75)
* restyle forgot your password as link (see #74)
* 5.7.0
* Upgrade jQuery 2.1.1 -> 2.1.3
* Upgrade Font Awesome 4.2.0 -> 4.3.0
* Upgrade bootstrap 3.3.0 -> 3.3.2
* Add <section> to subnav_base.html
* Pull in body, section and footer styles from pinax starter projects
* Explain error -> danger alias
* Handle instances where level_tag is undefined /  / Better mimics the implementation of message.tags in Django 1.7
* Allow for lazy translation of message tags
* Use level_tag to be consistent with Django >= 1.7
* Alias "error" as "danger", since .alert-error does not exist in Bootstrap 3
* Retrieve the message level tag and prefix it with alert-
* Retrieve message tags via get_message_tags template tag
* Add pinax_theme_bootstrap_tags tag library
