---
layout: post
title: "django-bitly 0.7 Release Notes"
date: 2013-04-12 16:05:10
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-bitly/django-bitly-0.7.tar.gz>

This release includes the following:

* optionally allow to specify http scheme
* remove unnecessary import
* allow multiple Bittles for instance
* added missing line in installation docs
* added Models API to the read me
* avoid querying for model instance's content type
* added Readme
* typo
* removed BITLY_FALLBACK_ABSOLUTE_URL. Too confusing.
* added timeout for bit.ly requests
* pep8
* bumped up minimum requirement for django
* added .gitignore
* ported example app to django 1.5
* raise more useful error message when bit.ly credentials are not set
* use timezone-aware datetimes if possible
* replaced catch-all except with error-specific one
* remove verify_exists parameters for Django 1.5 compatibility, fixes DiscoveryCreative/django-bitly#3
* stats request must be done in GET
* fixed typo /  / Signed-off-by: Flavio Curella <flavio.curella@gmail.com>
* bumped up version to 0.7 /  / Signed-off-by: Flavio Curella <flavio.curella@gmail.com>
* added a setting that allows bitlify filter to just return the absolute url in case BittleException is raised /  / Signed-off-by: Flavio Curella <flavio.curella@gmail.com>
