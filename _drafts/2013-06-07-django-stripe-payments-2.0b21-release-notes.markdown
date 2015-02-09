---
layout: post
title: "django-stripe-payments 2.0b21 Release Notes"
date: 2013-06-07 19:55:23
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-stripe-payments/django-stripe-payments-2.0b21.tar.gz>

This release includes the following:

* Fix bug where email receipt had scientific notation /  / >>> 40000 / decimal.Decimal("100") / Decimal('400') / >>> 40000 / decimal.Decimal("100.00") / Decimal('4E+2') /  / This seems to be corrected when saved and pulled / back out of the database, but went ahead and corrected / it across the board.
* Start documentation on model API
