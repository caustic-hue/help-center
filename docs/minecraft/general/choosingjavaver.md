---
layout: default
title:  "Choosing The Java Version"
parent: General
grand_parent: Minecraft
permalink: /minecraft/general/choosingjavaversion/
tags: minecraft java faq
---

# Choosing Your Server Java Version

## Minecraft 1.12 Or Lower

* Java8

## Minecraft 1.13 Or Higher

* Java11

# How To Make a Java Version The Default One

* Make sure your server is turned off before doing the next steps.

To make a Java version the default one, so that you don't need to select it every time you start your server, visit the [game panel](https://panel.falixnodes.net/), find and click on your server, find the "Startup" page on the top bar, scroll down to "Variables", then find "JAVA VERSION" and type the following for:

## Java8


`adopt@1.8.0-275`

## Java11


`adopt@1.11.0-9`


Now, go back to your console, start your server and you'll see it using the Java version you set.


* If the above does not work, manually delete the `.jabba` folder and restart your server.
