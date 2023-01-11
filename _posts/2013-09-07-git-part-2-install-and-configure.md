---
layout: post
title: 'গিট : ইন্সটল ও কনফিগার করা-পর্ব-২'
date: 2013-09-07 10:28:21.000000000 +06:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- গিট
- ভার্সন কন্ট্রোল সিস্টেম
tags: []
meta:
  _edit_last: '1'
  publicize_reach: a:2:{s:7:"twitter";a:1:{i:4514541;i:104;}s:2:"wp";a:1:{i:0;i:2;}}
  publicize_twitter_user: theazharul
  _wpas_done_4514541: '1'
  _publicize_done_external: a:1:{s:7:"twitter";a:1:{i:91116567;b:1;}}
  _last_editor_used_jetpack: block-editor
  _publicize_job_id: '68133230382'
  _jetpack_related_posts_cache: a:1:{s:32:"37550b67d263a3ce789993dc25046c5f";a:2:{s:7:"expires";i:1643268259;s:7:"payload";a:4:{i:0;a:1:{s:2:"id";i:7;}i:1;a:1:{s:2:"id";i:194;}i:2;a:1:{s:2:"id";i:112;}i:3;a:1:{s:2:"id";i:109;}}}}
author: azhar
permalink: "/"
---
<p>গিট নিয়ে কাজ শুরু করার জন্য আপনার কম্পিউটারকে গিট ব্যবহার উপযোগী করে নিতে হবে। সেজন্য আপনার কম্পিউটারে গিট ইন্সটল(install) করতে হবে। চলুন দেখে নেয়া যাক, কিভাবে গিট ইন্সটল এবং কনফিগার(configure) করে নিতে হয়।<br />
Windows:<br />
১. গিট প্যাকেজটি ডাউনলোড করার জন্য <a href="http://git-scm.com/download/win">এখানে ক্লিক করুন</a>।<br />
২. ডাউনলোড করা ফাইলটি ক্লিক করে ইন্সটল করে নিন।<br />
Linux:<br />
Linux এর বিভিন্ন ডিস্ট্রো এর জন্য গিট ইন্সটল পদ্ধতি বিভিন্ন রকম। কিন্তু খুবই সহজ। ডিস্ট্রো অনুযায়ী terminal-এ নিচের কমান্ডগুলো লিখুন।<br />
Debian/Ubuntu<br />
<code>$ apt-get install git</code><br />
Fedora<br />
<code>$ yum install git </code><br />
Gentoo<br />
<code>$ emerge --ask --verbose dev-vcs/git </code><br />
Arch Linux<br />
<code>$ pacman -S git </code><br />
FreeBSD<br />
<code>$ cd /usr/ports/devel/git<br />
$ make install </code><br />
Solaris 11 Express<br />
<code>$ pkg install developer/versioning/git </code><br />
OpenBSD<br />
<code>$ pkg_add git</code></p>
<p>গিট কনফিগার:<br />
গিট কনফিগার করার মূল উদ্দেশ্য হচ্ছে, আপনি যখন গিট এর মাধ্যমে কমিট(commit) করবেন তখন কমিটের সাথে সে আপনার তথ্য সংরক্ষণ করে রাখবে। কনফিগারেশনের সময় আপনাকে শুধু আপনার user name এবং email address বলে দিতে হবে।<br />
Windows ব্যবহারকারীরা<br />
গিট ইন্সটল করার পর কম্পিউটার ডেক্সটপে gitBash নামে একটি শর্টকাট ফাইল তৈরি হবে। সেটি খুলে তাতে নিচের কমান্ডগুলো লিখুন। Linux ব্যবহারকারীরা terminal-এ কমান্ডগুলো লিখতে পারবেন।<br />
<code>git config --global user.name "Your Name Here"</code><br />
Your Name Here এর জায়গায় আপনার নাম লিখুন।<br />
<code>git config --global user.email "your_email@youremail.com"</code><br />
এখানে যে email address দিবেন তা অবশ্যই আপনার সার্ভার অ্যাকাউন্টের email address এর সাথে মিল থাকতে হবে।<br />
এখন আপনার কম্পিউটারটি গিট ব্যবহার উপযোগি হয়েছে। এখন থেকে আপনি আপনার কম্পিউটারে গিটের কমান্ডগুলো কাজে লাগাতে পারবেন।<br />
আমরা আমাদের সকল কমান্ড gitBash অথবা terminal-এ লিখবো।</p>
