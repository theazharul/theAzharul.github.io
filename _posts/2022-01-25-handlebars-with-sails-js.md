---
layout: post
title: Sails.js এর সাথে Handlebars ব্যবহার করা
date: 2022-01-25 13:11:30.000000000 +06:00
type: post
parent_id: "0"
published: true
password: ""
status: publish
categories:
  - ওয়েব ডেভেলপমেন্ট
tags: []
meta:
  _last_editor_used_jetpack: block-editor
  _wpas_done_4514541: "1"
  publicize_twitter_user: theazharul
  _publicize_job_id: "68133379744"
  timeline_notification: "1643116294"
  _publicize_done_external: a:1:{s:7:"twitter";a:1:{i:4514541;s:57:"https://twitter.com/theazharul/status/1485963559389519878";}}
  _publicize_done_4607822: "1"
  _edit_last: "1"
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1648352821;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:7;}i:1;a:1:{s:2:"id";i:194;}i:2;a:1:{s:2:"id";i:123;}}}}
  _thumbnail_id: "229"
  _yoast_wpseo_content_score: "90"
  _yoast_wpseo_estimated-reading-time-minutes: "1"
author: azhar
---

Node.js এর জনপ্রিয় ফ্রেমওয়ার্ক Sails.js এর সাথে টেমপ্লেট ইঞ্জিন হিসেবে ejs দেয়া থাকে। তবে আমরা চাইলে ejs এর পরিবর্তে handlebars ব্যবহার করতে পারি।

প্রথমেই আপনার কম্পিউটারে Sails.js ইন্সটল করে নিন-

npm -g install sails

Sails.js এর সাথে Handlebars ব্যবহার করার জন্য আমাদেরকে প্রথমেই sails-generate-views-handlebars নোড প্যাকেজটি ইন্সটল করে নিতে হবে। সেজন্য নিচের কমান্ডটি দিন-

‌‌‌npm install sails-generate-views-handlebars -g‌‌

এর পর নিম্নোক্ত কমান্ড দিয়ে একটি নতুন Sails.js প্রজেক্ট তৈরি করে নিন।

sails new <project-name> --template=handlebars

এর পরিবর্তে আপনার প্রজেক্টের নামটি ব্যবহার করতে হবে।

এখন আপনি আপনার প্রজেক্টের config/view.js ফাইলে গেলে দেখবেন ‌‌‌engine: ‘handlebars’ দেখাচ্ছে।

Congratulation! আপনার Sails.js প্রজেক্টের সাথে টেমপ্লেট ইঞ্জিন হিসেবে ejs এর পরিবর্তে handlebars সংযুক্ত হয়ে গেছে।

তবে আর একটু ধৈর্য্য ধরতে হবে :P ।

আপনার config/view.js ফাইলের

layout: 'layouts/layout.handlebars'

লাইনটা পরিবর্তন করে

layout: 'layouts/layout'

করে দিতে হবে।

এখন আপনার টার্মিনালে

sails lift

কমান্ড দিয়ে ব্রাউজারে [http://localhost:1337/](http://localhost:1337/) দিলেই আপনার সাইটটি দেখতে পাবেন।

আরো একটা সমস্যা রয়ে গেছে। আমরা সাধারণত Sails.js প্রজেক্টের assets/js এবং assets/styles ফোল্ডারে যথাক্রমে জাভাস্ক্রিপ্ট এবং সিএসএস ফাইলগুলো রাখলেই সেগুলো সরাসরি লেআউট ফাইলে সংযুক্ত হয়ে যাওয়ার কথা। কিন্তু টেমপ্লেট ইঞ্জিন হিসেবে handlebars ব্যবহার করার কারনে সেটা আর হচ্ছে না। এই সমস্যা থেকে উত্তরণের জন্য আমাদেরকে ছোট্ট একটা কাজ করতে হবে।

tasks/config/sails-linker.js ফাইলের যত .ejs আছে সেগুলোকে .handlebars দিয়ে রিপ্লেস করতে হবে।

ব্যস, এবার মনের খুশিতে আপনার Sails.js প্রজেক্টের সাথে handlebars ব্যবহার করুন। :)
