---
title: Hybrid Join vs AAD Join
description: 
published: true
date: 2022-09-30T12:58:05.462Z
tags: 
editor: markdown
dateCreated: 2022-09-30T11:20:45.613Z
---

## When should you use HAADJ?

* HAADJ is fine for your existing, already domain-joined devices.
* There's no reason not to enable hybrid join for all existing domain-joined devices.
* Anything you continue to image for "reasons" in a traditional process should end up hybrid-joined.
* You need device-based Kerberos auth and you can't replace it with certificates.
* You have 802.1x infrastructure relying on computer objects in AD.

## Why shouldn't you use HAADJ

* Hybrid Autopilot is actually pretty easy to set up and get working (at least on-premises without VPN), but do you really need to do it? No, you most likely don't.
* Continue to provision old devices using existing processes, and only build new processes for things that will stay around.
* Why waste the time implementing Hybrid AAD if it will eventually go away, once everything is AADJ?

## When should you use Azure AD Join?

* Azure AD join is the preferred choice going forward
* Any user assigned device deployed via Autopilot should be user-driven Azure AD-only 99% of the time.

## External Links

* [To AAD Join or Not … That is the Question](https://techcommunity.microsoft.com/t5/core-infrastructure-and-security/to-aad-join-or-not-that-is-the-question/ba-p/3435768)
