---
layout: post
title:  "Musibah Gitlab: Yang Perlu Kita Pelajari"
date:   2017-02-02 14:00:00 +0530
comments: true
---
![gitlab](https://pbs.twimg.com/card_img/826584326758215680/IwSTiXlp?format=jpg&name=386x202)

Gitlab, perusahaan yang bergerak di bidang developer tools, dengan tagline "GitLab unifies issues, code review, CI and CD into a single UI", merupakan sebuah repository untuk merancang sistem mirip dengan Github. Tentunya dengan fitur-fitur andalan pada mode premium, Gitlab memberikan pengalaman yang menarik untuk mengembangkan sistem. Oke, itu intro :D

Kemarin hari (01 Febuari 2017), musibah tiba-tiba datang dan meradang Gitlab hingga situsnya tidak bisa diakses. Insiden terjadi pada salah satu database diantara empat database data mereka (issues, merge requests, users, comments, snippets, dll). Tidak tanggung-tanggung, selama 6 jam Gitlab mengalami kegagalan sistem dan yang paling berdampak, yakni production data.

Teknisi Gitlab menduga, serangan pertama memukul database mereka dengan cara spamming database dengan membuat snippet, membuat sistem tidak stabil.

![Spamming Snippets](https://about.gitlab.com/images/db_incident/snippets.png)

Serangan menghempas tiga kali sebelum tahap recovery dimulai. Beberapa kesimpulan pun dibuat, dari snapshot yang berjalan pada siklus 24 jam-an hingga Amazon S3 yang ternyata tidak mem-backup data. 

Lebih lengkapnya baca di web mereka, sebuah insiden yang pedih mungkin bisa jadi pelajaran bagi kita :)

![Link](https://about.gitlab.com/2017/02/01/gitlab-dot-com-database-incident/)

> Seperti cinta, kegagalan sistem acapkali terjadi diluar dugaan kita, waspada! -MRS
