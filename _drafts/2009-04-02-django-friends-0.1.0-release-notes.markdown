---
layout: post
title: "django-friends 0.1.0 Release Notes"
date: 2009-04-02 03:52:40
categories: release-notes
---

Download: <https://pypi.python.org/packages/source/d/django-friends/django-friends-0.1.0.tar.gz>

This release includes the following:

* Added simple setup.py /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@58 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Moved django-friends on level up in preparatio for a release /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@57 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added missing close tag in join accept notice /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@56 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* renamed notification templates /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@55 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* fixed relative import /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@54 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* fixed typo that prevented otherconnect notices working on join invitation accept /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@53 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Avoid many calls to notification.send in JoinInvitation.accept for friends_otherconnect. /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@52 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Removed use of captureas template tag in default notification templates /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@51 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* yahoo import no longer crashes on missing first or last name /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@50 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* improved friends_invite notifications /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@49 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* improved notification message on friend request acceptance /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@48 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Made use of select_related when building a list of friends in friends_for_user in FriendshipManager. This makes use of an INNER JOIN to prevent extra queries on the data set. /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@47 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* avoid integrity violation by only accepting invitation if not already friends /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@46 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Updated signals code due to backwards incompatible change in Django r8223 /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@45 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* fixes for plain.txt notification templates /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@44 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* fixed more of notification templates /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@43 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* fixed plain.txt /  /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@42 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* fixes for blocktrans misuse /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@41 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Removed reference to newforms. /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@40 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Fixed up project to be compatible with NFA version of trunk. /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@39 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added teaser.html files for the new notification api and made some changes to the passed variables /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@38 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* marked notification descriptions as translateable /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@37 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* initial pass at port to new notification templates -- plain.txt only now and no extra information beyond old notification messages yet /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@36 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added field on Contact for which user(s) the contact correspond to if any /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@33 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* update join_invitation status when an invited user joins independently /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@32 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* use new get_users_for(email) method /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@31 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* support for names in Google contact import /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@30 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added google contacts importer /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@29 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added yahoo address book importer /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@28 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* only add contacts that aren't duplicates /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@27 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added default /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@26 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* removed unnecessary import /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@25 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Pass along the full URL constructed from contrib.sites and reverse to the accept_join view. /  /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@24 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Added a missing import. /  /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@23 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Moved the hardcoded join invite email to templates. /  /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@22 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* implemented join invitation accept with notification /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@21 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* include from_user field on join invitation and include message in email /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@20 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* populate existing_users attribute on join invitation form /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@19 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Updated calls to django-notifications to work with the slightly revised API. /  /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@18 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* first part of join invitation -- you can sent join invitations but nothing accepts them yet /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@17 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* changed creation of notification to support new message templates /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@16 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* new notification types: sent/receive distinction plus new other connect notice /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@15 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* update for changes in django-notification r9 /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@14 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* fixed typo in notification message /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@13 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added initial support for django-notification /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@12 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added are_friends method to Friendship manager and accept method to FriendshipInvitation model /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@11 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* now check for existing invitations in both directions /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@10 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* form for requesting friendship /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@9 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added manager with method for retrieving friends of given user /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@8 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* used default functions rather than overriding save to add creation dates /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@7 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added Admin classes with list_display /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@6 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* switched to using max_length: Issue 2 /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@5 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* added svn:ignore /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@4 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* typo in doc /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@3 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* initial model, including contacts, friends and invitations; vcard import utility /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@2 f9456ae0-1038-0410-abc2-2f1ed958ef3d
* Initial directory structure. /  / git-svn-id: http://django-friends.googlecode.com/svn/trunk@1 f9456ae0-1038-0410-abc2-2f1ed958ef3d
