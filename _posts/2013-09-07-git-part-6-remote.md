---
layout: post
title: "গিট : একাধিক রিমোট রিপোজিটরির সাথে সংযোগ-পর্ব-৬"
date: 2013-09-07 10:37:08.000000000 +06:00
type: post
parent_id: "0"
published: true
password: ""
status: publish
categories: [প্রোগ্রামিং]
tags: [গিট, ভার্সন কন্ট্রোল সিস্টেম]
meta:
  _last_editor_used_jetpack: block-editor
  _edit_last: "1"
  publicize_twitter_user: theazharul
  _wpas_done_4514541: "1"
  _publicize_done_external: a:1:{s:7:"twitter";a:1:{i:91116567;b:1;}}
  _publicize_job_id: "68133288126"
  _jetpack_related_posts_cache: a:1:{s:32:"8f6677c9d6b0f903e98ad32ec61f8deb";a:2:{s:7:"expires";i:1643807545;s:7:"payload";a:3:{i:0;a:1:{s:2:"id";i:7;}i:1;a:1:{s:2:"id";i:123;}i:2;a:1:{s:2:"id";i:194;}}}}
author: azhar
---

একই রিপোজিটরিতে একাধিক ডেভেলপার কাজ করলে একজন ডেভেলপার অন্য একজন ডেভেলপারের কাজ pull করার প্রয়োজন হতে পারে। এছাড়াও admin যখন কোন ডেভেলপারের কাজ পর্যবেক্ষণ করবেন তখন ঐ ডেভেলপারের রিপোজিটরির সাথে admin এর রিপোজিটরির সংযোগ দিতে হবে। চলুন দেখে নেয়া যাক কিভাবে রিমোট রিপোজিটরির সাথে সংযোগ দেয়া যায়।  
রিমোট রিপোজিটরির সাথে সংযোগ দেয়ার জন্য আমাদেরকে git remote কমান্ডটি ব্যবহার করতে হবে। সম্পূর্ণ কমান্ডটি নিচে দেয়া হলো-  
`git remote add name server-address`  
এখানে name এর জায়গায় আপনি রিমোট রিপোজিটরিটিকে যে নামে ডাকতে চান সে নাম হবে। server-address এর জায়গায় রিমোট রিপোজিটরিটির address দিতে হবে।  
ধরুন আমরা একটি কেন্দ্রীয় রিপোজিটরি তৈরি করলাম যার নাম হচ্ছে rms এবং রিপোজিটরিটির address হচ্ছে [https://bitbucket.org/precursortechnology/rms.git](https://bitbucket.org/precursortechnology/rms.git) । এখন এতে যতজন ডেভেলপার কাজ করবে সবাই এই রিপোজিটরিটি fork করতে হবে (fork সম্পর্কে জানতে [দেখুন](http://www.techtunes.com.bd/internet/tune-id/178340))। এখন ডেভেলপাররা যদি তাদের রিপোজিটরিকে কেন্দ্রীয় রিপোজিটরির([https://bitbucket.org/precursortechnology/rms.git](https://bitbucket.org/precursortechnology/rms.git)) সাথে সংযোগ দিতে চান তাহলে তাদেরকে লিখতে হবে  
`git remote add upstream [https://bitbucket.org/precursortechnology/rms.git](https://bitbucket.org/precursortechnology/rms.git)`  
এখানে আমরা কেন্দ্রীয় রিপোজিটরিকে চেনার জন্য upstream নাম ব্যবহার করেছি। আপনি চাইলে অন্য যে কোন নাম ব্যবহার করতে পারেন। এখন কোন ডেভেলপার যদি কেন্দ্রীয় রিপোজিটরির তথ্য pull করতে চান তাহলে তাকে লিখতে হবে  
`git pull upstream master`  
pull করে মানে হচ্ছে ঐ রিপোজিটরির সর্বশেষ আপডেটগুলো আপনার রিপোজিটরির সাথে একীভূত করে নেয়া। pull কমান্ড দিয়ে মূলত দুটি কাজ করা হয়। প্রথমে রিমোট রিপোজিটরিটির তথ্যগুলো fetch করে নেয়া হয় এবং পরে সেগুলো লোকাল রিপোজিটরির সাথে merge করা হয়। উপরের কমান্ড দিয়ে আমরা upstream নামক রিমোট রিপোজিটরির master branch(ব্রাঞ্চ নিয়ে অন্য টিউটরিয়ালে আলোচনা করা হবে)-এর সাথে নিজেদের repository merge করে নিলাম।  
admin যদি কোন ডেভেলপারের সাথে সংযুক্ত হতে চান তাহলে তাকেও উপরের ধাপগুলো অনুসরণ করতে হবে।  
একটি রিপোজিটরি চাইলে একাধিক রিমোট রিপোজিটরির সাথে সংযুক্ত হতে পারবে।
