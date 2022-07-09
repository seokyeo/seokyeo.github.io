---
title: "playlist"
layout: archive
permalink: categories/playlist
author_profile: true
sidebar_main: true
---


{% assign posts = site.categories.playlist %}
{% for post in posts %} {% include archive-single2.html type=page.entries_layout %} {% endfor %}