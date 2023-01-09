---
layout: post
title: "Mac অপারেটিং সিস্টেমে Emacs ইন্সটল করা"
author: azhar
categories: [Emacs, Mac]
image: assets/images/emacs/emacs-logo.jpg
featured: true
---

আমরা Mac-এ গ্রাফিকাল ইউজার ইন্টারফেসসহ Emacs পাওয়ার জন্য Homebrew-Emacs-Plus ইন্সটল করে নেবো। সেজন্য টার্মিনালে নিচের কমান্ডগুলো লিখবো-

`$ brew tap d12frosted/emacs-plus`  
`$ brew install emacs-plus`

আমাদের Emacs ইন্সটল করা হয়েছে। এখন আমরা টার্মিনালে emacs লিখলে টার্মিনালে Emacs প্রদর্শণ করবে। কিন্তু Launchpad থেকে Emacs ওপেন করার জন্য Emacs অ্যাপটাকে Applications ফোল্ডারে লিংক করে দিতে হবে। সেজন্য আমরা টার্মিনালে লিখবো-

`$ ln -s /usr/local/opt/emacs-plus@27/Emacs.app /Applications`

এই কমান্ডটি আমরা emacs-plus ইন্সটল করার পর টার্মিনাল Info এর মধ্যে দেখতে পাবো। ভার্সনভেদে কমান্ড ভিন্ন রকমও হতে পারে যা আমরা টার্মিনালেই দেখতে পাবো।

এখন আমরা Launchpad থেকেই Emacs ওপেন করতে পারবো।
