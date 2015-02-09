---
layout: post
title: "django-trust 0.2 Release Notes"
date: 2012-07-29 22:24:30
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-trust/django-trust-0.2.tar.gz>

This release includes the following:

* Increase version
* Don't make it an error to not implement a certain TrustApp method
* Remove unused import
* Only run the trust code if we are processing it
* Fix an error where we were using TrustItem instead of obj
* Add the ability for an item to be requeued
* Added a simple example project
* Add a quued field to allow requeing already rated /  / When resubmitting an item to the queue the item will already have / a rating and thus will fail the rating=None check. This field will / allow a simple boolean as an additional check if an item has been / queued.
