---
layout: post
title: "pinax-theme-bootstrap 5.5.0 Release Notes"
date: 2014-08-11 03:12:33
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/p/pinax-theme-bootstrap/pinax-theme-bootstrap-5.5.0.tar.gz>

This release includes the following:

* Importing of settings is required for AppConf
* v5.5.0
* Remove outdated bits
* Upgrade jQuery from 1.8.3 to 2.1.1 /  / NOTE: This is a major upgrade. It should work just fine for all modern / browsers. The most significant thing that this will break is support for / older IE browsers. If you still need to support these browsers you can / override the `jquery_src` block and supply an version from the 1.x line.
* Upgrade less.js (1.7.0 ==> 1.7.3)
* Upgrade Bootstrap (3.1.1 ==> 3.2.0)
* Merge branch 'master' of github.com:pinax/pinax-theme-bootstrap
* select both id and class for account_logout
* FIX: pagination template with THOUSAND_SEPARATOR /  / Fixes incorrect urls in pagination templates when THOUSAND_SEPARATOR is / used, ie: ?page=1.000 /  / Also do not use THOUSAND_SEPARATOR when displaying page numbers.
* swapped account / setting #72
* make subnav base 3/9 not 2/10 #73
* copyright year
* PEP8 nits
* removed legacy templates #76
* rmoved banner_base and less_base #77
