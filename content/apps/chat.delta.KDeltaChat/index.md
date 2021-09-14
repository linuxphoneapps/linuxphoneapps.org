+++
title = "KDeltaChat"
description = "DeltaChat client built with Kirigami"
date = "2021-09-04"
updated = "2021-09-11"
author = "1peter10" # Original reporter
template = "apps/page.html"
[taxonomies]
mobile_compatibilities = ["5"]
frameworks = ["Kirigami"]
project_licenses = ["GPL-3.0-or-later"] # SPDX 3-0 identifier
services = ["deltachat"] 
backends = ["libdeltachat"] 
categories = ["messenger"]
freedesktop_categories = ["Qt","KDE","Network","Chat",]
build_systems = ["cmake"]
programming_languages = ["C++","QML",]
state = ["WIP"]
[extra]
### URLs
repository = "https://git.sr.ht/~link2xt/kdeltachat"
homepage = ""
bugtracker = ""
donation = ""
translate = ""
repology = ["kdeltachat"] # array
flathub = ""
flatpak_json_url = "" # not used yet, fill anyway please
app_id = "chat.delta.KDeltaChat"
# summary variable is in page.description (below title) for technical reasons (https://github.com/linuxphoneapps/linuxphoneapps.org/issues)
summary_source_url = "https://git.sr.ht/~link2xt/kdeltachat"
# description is below in page content
description_source_url = "" # Don't fill if editorial
icon_url = "" # not used yet, fill anyway please
notice = "No release yet, but works for simple, encrypted text conversations. Sending attachments (images etc.) is not implemented yet, received images aren't scaling properly. Adding an account works via importing a backup or the add account screen. <br> Compiling the necessary libdeltachat library takes a long time and requires more than 3GBs of RAM (at 4 threads) - doing this on device (PinePhone, Librem 5) is not recommended." # can be markdown, use <br> for line breaks
scale-to-fit = "" # Only fill where necessary
license_url = "https://git.sr.ht/~link2xt/kdeltachat/tree/master/item/LICENSE"
appstream_xml_url = ""
listing_contributors = [""] # Further contributors (array)
+++
