# SAMPLE for Index fn. Note: The filename is index for HTML reasons, not because of the app name. The folder name is the appid, when there's none, we'll use noappid.appname as a place holder. 
# Once the project adopts a (new) app id, an alias must be added, so that previous links don't break.
# 
# TODO: Check identifiers against appstream.xml /metainfo.xml specifications to make work on a future parser easier!
+++ 
title = "Index"
date = "2019-02-01"
updated = "2021-05-04"
[taxonomies]
mobile-compability = ["5"]
framework = ["MauiKit", "Kirigami"]
licenses = ["SPDX"]
services = 
backends =
categories = 
free-desktop-categories =
[extra]
repository = "https://invent.kde.org/kde/index-fm"
app_id = "org.kde.index"
summary = "Multi-platform file manager"
summary_url = "{{ page.extra.repository }}"
description = "Index is a file manager that works on desktops, Android and Plasma Mobile. Index lets you browse your system files and applications and preview your music, text, image and video files and share them with external applications."
summary_source_url = "{{ page.extra.repository }}"
website = ""
icon_url = "https://invent.kde.org/maui/index-fm/-/raw/master/logo.png" 
# scale-to-fit = "" # Only fill where necessary
license_url = "https://invent.kde.org/maui/index-fm/-/blob/master/LICENSES/GPL-3.0-or-later.txt" # because it's sometimes complicated
appstream_xml_url = "https://invent.kde.org/maui/index-fm/-/blob/master/org.kde.index.appdata.xml"
+++

# Notice

The text will be mostly non-existent, as the front-matter should get everything done: The template does the rest. 
It could be used for manual linking of "similar apps", as we won't have any automation for that.
