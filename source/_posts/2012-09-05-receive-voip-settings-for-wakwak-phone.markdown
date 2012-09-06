---
layout: post
title: "Receive VoIP settings for WAKWAK Phone"
date: 2012-09-05 22:53
comments: true
categories: VoIP WAKWAK
---

WAKWAK that is a ISP provides IP phone, the free to deal, by the name of ["WAKWAK Phone"](http://www.wakwak.com/service/phone/).
It need to have a IP phone that is implemented "voip-setup.cgi" as root of HTTP.
But I want to save VoIP's settings into a router,
so I made [receive VoIP's settings software](https://github.com/aycabta/wakwakphone).

Approach
--------

1. Clone code from GitHub
    * {% gist 3653287 %}
2. Run receive VoIP's settings software
    * {% gist 3653313 %}
3. Access to WAKWAK Online User Support
4. Reconfigure terminal infomation
    * {% img ./reconfigure.png %}
5. Save terminal configuration password
6. Receive e-mail that is written the configuration URL
7. Access the URL, maybe it likes "*https://cust.lmc.xephion.ne.jp:48443/xcpvcs/index.html?id=0123456789ABCDEF0123456789ABCDEF0123456789ABCD*"
8. Automatically be redirected to "*https://cust.lmc.xephion.ne.jp:48443/xcpvcs/servlet/IADURLParseAndSetServlet?id=0123456789ABCDEF0123456789ABCDEF0123456789ABCD*" by JavaScript if URL above
9. Input the configuration password that is saved
    * {% img ./password-is-required.png %}
10. Input "machine:8989" and submit, "machine" is your machine's IP address or hostname
    * {% img ./run-configuration.png %}
    * Settings is written in hidden parameter in this page
11. Look at logs of receive VoIP's settings software, settings is outputed
    * {% gist 3653353 %}

