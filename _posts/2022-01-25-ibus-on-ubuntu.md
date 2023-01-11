---
layout: post
title: উবুন্টুতে Ibus দিয়ে বাংলা লিখতে না পারলে
date: 2022-01-25 13:12:46.000000000 +06:00
type: post
parent_id: "0"
published: true
password: ""
status: publish
categories:
  - Operating System
tags: []
meta:
  _last_editor_used_jetpack: block-editor
  publicize_twitter_user: theazharul
  timeline_notification: "1643116371"
  _publicize_job_id: "68133420899"
  _publicize_done_external: a:1:{s:7:"twitter";a:1:{i:4514541;s:57:"https://twitter.com/theazharul/status/1485963880555819012";}}
  _publicize_done_4607822: "1"
  _wpas_done_4514541: "1"
  _edit_last: "1"
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1648284402;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:109;}i:1;a:1:{s:2:"id";i:194;}i:2;a:1:{s:2:"id";i:7;}}}}
  _thumbnail_id: "225"
  _yoast_wpseo_content_score: "90"
  _yoast_wpseo_estimated-reading-time-minutes: "1"
author: azhar
permalink: "/"
---

যারা ubuntu 16.04 ভার্সনে আপগ্রেড করেছেন তারা ibus-m17n প্যাকেজটা দিয়ে বাংলা লিখতে সমস্যায় পড়ে যান। xubuntu, lubuntu এই ভার্সনের ডিস্ট্রোগুলোতেও এই সমস্যাটা করে। এই সমস্যা সমাধান করার জন্য ছোট্ট একটা কমান্ড দিলে আশা করি বাংলা ঠিকভাবে কাজ করবে। কমান্ডটা হচ্ছে-

sudo apt-get install ibus-m17n ibus-gtk ibus-gtk3
