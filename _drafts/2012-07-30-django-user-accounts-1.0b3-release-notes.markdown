---
layout: post
title: "django-user-accounts 1.0b3 Release Notes"
date: 2012-07-30 22:40:30
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-user-accounts/django-user-accounts-1.0b3.tar.gz>

This release includes the following:

* SECURITY FIX: fixed default_redirect to prevent XSS attack /  / Discovered in django.contrib.auth it is possible for an attack to craft a / specific URL using ?next to execute arbitrary Javascript within the victim's / browser. /  / We now only redirect if the URL scheme is allowed and it matches the allowed / host (based off of request.get_host() by default.) You are able to pass in / custom overrides to these options using get_success_url methods.
