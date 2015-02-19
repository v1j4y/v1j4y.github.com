---
layout: post
title: "how to get jackd working with USB sound card"
description: ""
category: programming
tags: [jackd,overtone,clojure,vimclojure]
---
{% include JB/setup %}

Install jackd,qjackctl,jack-tools

    sudo apt-get install jackd qjackctl jack-tools

jackd server can be started usually with the command

    pulseaudio -k
    jack_control start

In my case this did now work as the sound card was initialized
as hw:1 instead of hw:0

In order to get a minimal working version of overtone, do this

    sudo jackd -R -d alsa -d hw:1,0

followd by lauching lein as root as well


    sudo lein vimclojure

Normally this would make lein use the running instance of jackd 
previously started and configured to use the USB devise.
