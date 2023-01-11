---
layout: post
title: উবুন্টুতে Ibus দিয়ে বাংলা লিখতে না পারলে
type: post
categories: [Operating System]
tags: []
author: azhar
---

যারা ubuntu 16.04 ভার্সনে আপগ্রেড করেছেন তারা ibus-m17n প্যাকেজটা দিয়ে বাংলা লিখতে সমস্যায় পড়ে যান। xubuntu, lubuntu এই ভার্সনের ডিস্ট্রোগুলোতেও এই সমস্যাটা করে। এই সমস্যা সমাধান করার জন্য ছোট্ট একটা কমান্ড দিলে আশা করি বাংলা ঠিকভাবে কাজ করবে। কমান্ডটা হচ্ছে-

sudo apt-get install ibus-m17n ibus-gtk ibus-gtk3
