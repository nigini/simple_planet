simple_planet
=============

A personal "toy project"! Searching to learn more about Python and Django programming, I thought of creating a personal site, that would aggregate my social feeds. To practice, I want to implement firstly a simple planet platform as the ones I've found were broken at first tries.

How to use it?
====

I'm developing this using Python 2.7 and Django 1.4.
Project requirement is the feedparser (http://code.google.com/p/feedparser/) that can be installed with pip.

You should create your Django project (please activate admin) and add simple_planet as an APP. Another modification is that the template folder available at simple_planet root have to be inserted at your template diretory with the name planet. With this you will probably be able to execute syncdb and runserver to make some tests.

If it is right, you'll be able to use admin to add a RSS feed. Take for example the great "Daily Dilbert Strip": http://feed.dilbert.com/dilbert/daily_strip

Given that a Planet should populate your posts based on the available feeds. It's probably a periodic task that can be inserted for example in a CRON tab to be executed daily. As a test I wrote the simple_planet.views.add_posts() that will luckly parse feeds and add your posts! BE AWARE that it is not checking for post duplication yet!
