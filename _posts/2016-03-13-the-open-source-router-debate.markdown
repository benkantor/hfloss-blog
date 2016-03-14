---
layout: post
title:  "The Open Source Router Debate"
date:   2016-03-13 20:30:00
categories: blog
---
If you've ever used a consumer grade router, you may have found the software to
be diffcult used and lacking customization. As a response to this, several free
and open source router firmware projects ([OpenWRT][openwrt] and
[DD-WRT][ddwrt] being the most popular) have grown inpopularity due to their
ability to improve performance and overall customization.

Back in September 2015, the FCC announced new security restrictions for certain
hardware device such as wirless routers to ensure that they couldn't be
modified to operate outside of the 5Ghz band in which they are legally allowed
to operate. The decision to increase security came after the FAA discovered
that illeglaly modified hardware was being used to interfer with dopler weather
radar at airports.

The FCC announcement sparked strong concern in the open source community as the
proposed rules mention that hardware manufacturers must be able to explain how
they are able to prevent third party software, specifically DD-WRT from being
able to modify the power output of thier devices. The main reason for concern
of third party firmware is that currently most manufacturers don't place
hardware restriction on their devices. The FCC has said that they don't want to
ban third party software from being installed, however they are leaving it up
to Companies to decided how they will restrict modifications whether it be at
the software or harware level.

As several developers of open source firmware have pointed out, it is very
likely that hardware manufacturers will simply just restrict the ability for
third party firmware to be installed as it is much cheaper than creating
developing new hardware with restrictions.

This week those predicitions began to prove true as networking hardware
manufacturer [TP-Link][tp-link] announced that it will placing restricions on
its products that will prevent users from flashing current versions of third
party firmware. In their defense, TP-Link has never provided official support
for installing third party firmware and it would be hard to determine their
section of their users who flash third party firmware.

So what does this mean for people who want to use third party firmware? If
other major manufacturers follow the path of TP-Link, consumers will most
likely have to spend more money on niche hardware manufacturers that support
hardware restrictions. While the new regulations may be stifiling FOSS
software, the increased limitations of commecial hardware could lead to an
increases interest in the development of Open Source hardware.

[ddwrt]: http://www.dd-wrt.com/site/index
[openwrt]: http://wiki.openwrt.org/about/start
[tp-link]: http://arstechnica.com/information-technology/2016/03/tp-link-blocks-open-source-router-firmware-to-comply-with-new-fcc-rule