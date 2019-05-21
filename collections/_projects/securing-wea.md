---
layout: headlines_layout
title: Securing LTE Emergency Alerts
caption: Mobile and wireless security
date: 05/13/2019
permalink: /projects/securing-wea.html
---

<!--
Add pic2
-->


## Securing LTE Emergency Alerts

Modern cell phones are required to receive and display alerts via the Wireless Emergency Alert (WEA) program, under the mandate of the Warning, Alert, and Response Act of 2006. These alerts include AMBER alerts, severe weather alerts, and (unblockable) Presidential Alerts, intended to inform the public of imminent threats. Recently, a test Presidential Alert was sent to all capable phones in the United States, prompting concerns about how the underlying WEA protocol could be misused or attacked. In this paper, we investigate the details of this system, and develop and demonstrate the first practical spoofing attack on Presidential Alerts, using both commercially available hardware as well as modified open source software. Our attack can be performed using a commercially-available software defined radio, and our modifications to the open source NextEPC and srsLTE software libraries. We find that with only four malicious portable base stations of a single Watt of transmit power each, almost all of a 50,000-seat stadium can be attacked with a 90\% success rate. The true impact of such an attack would of course depend on the density of cell phones in range; fake alerts in crowded cities or stadiums could potentially result in cascades of panic.

Fixing this problem will require a large collaborative effort between carriers, government stakeholders, and cell phone manufacturers. To seed this effort, we also discuss several defenses to address this threat in both the short and long term. 


## Publications

***This is Your President Speaking: Spoofing Alerts in 4G LTE Networks***
by Gyuhong Lee, Jihoon Lee, Jinsung Lee, Youngbin Im, Max Hollingsworth, Eric Wustrow, Dirk Grunwald, and Sangtae Ha (University of Colorado Boulder) was accepted to MobiSys 2019.

## Video

[![cmas_video](https://img.youtube.com/vi/XJ7FPYs2bIw/0.jpg)](https://www.youtube.com/watch?v=XJ7FPYs2bIw)
