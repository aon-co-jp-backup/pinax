---
layout: post
title: "django-avatar 1.0.3 Release Notes"
date: 2009-11-07 19:32:49
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-avatar/django-avatar-1.0.3.tar.gz>

This release includes the following:

* bumped version
* added CHANGELOG
* Check for django-friends using INSTALLED_APPS to prevent imports from happening /  / Reported to Pinax as http://code.pinaxproject.com/tasks/task/481/ /  / Signed-off-by: Brian Rosner <brosner@gmail.com>
* Removed setuptools install_requires (definitely not needed)
* removed new_primary from views.py delete method /  / Signed-off-by: Eric Florenzano <floguy@gmail.com>
* Added notification templated. Can't verify that they are being used. / new_primay wasn't being used in delete_avatar /  / Signed-off-by: Eric Florenzano <floguy@gmail.com>
* Added avatar_updated and avatar_friend_updated /  / Signed-off-by: Eric Florenzano <floguy@gmail.com>
* Set a new primary avatar when deleting the primary avatar. /  / Signed-off-by: Eric Florenzano <floguy@gmail.com>
* Added manifest template, package_data and bumped to 1.0.2 /  / Signed-off-by: Brian Rosner <brosner@gmail.com>
* Added manifest template, package_data and bumped to 1.0.2
* Removed some legacy code that is no longer used. Closes #1. /  / Due to catching the User post_save signal this would be fired on each login / since last_login is always updated.
* Removed usage of hashlib to support Python 2.4. /  / git-svn-id: http://django-avatar.googlecode.com/svn/trunk@36 c76b2324-5f53-0410-85ac-b1078a54aeeb
