---
layout: headlines_layout
title: Resilient Communications
caption: Ongoing work funded by Public Safety Communications Research
date: 12/1/2001
permalink: /projects/pscr.html
---


## Overview 

The proposal uses commodity networks, including
WiFi, Bluetooth, commercially available UHF radios and LTE networks to evaluate
a proposed software environment
***respons***, the **R**eliable **E**nvironment for **S**ecure 
 **P**olice **O**perations and **N**etworks.
This portion of the proposed work seeks to
develop a usable fog computing application environment
for use in dispersed or situational computing
for police systems. The ***respons*** system uses a combination of
distributed consensus systems, distributed transactional memory and
object systems, multi-path routing and container-based application
isolation. Many of the technologies needed for resilient systems are
commonly used in existing datacenter scale systems, but those systems
require adaptation for the relatively poor network connectivity and
disconnected operation that would occur in field systems.
Reusing the existing software and design patterns simplifies the
training needed to develop applications using the software framework.
This system will use the plurality of networks which can be
partitioned and perturbed to emulate network partitions and failures,
and consumer-grade long-range but low-bandwidth networks used to
emulate functions of the emerging device-to-device networking
standard.

This proposal is funded by NIST [Public Safety Communications
Research](https://www.nist.gov/communications-technology-laboratory/pscr). 



## Mobile Edge Computing over Elastic EPC cluster

Mobile Edge Computing (MEC) is an essential part of the 5G plan to support the numerous IoT devices that are projected
to be in use over the coming decades. These IoT devices will have very limited computing power and will rely on services
provided from the network to process and respond to the physical input they are receiving. We believe that there is
utility in taking inspiration from MEC in 5G and applying it to public safety communications. Latency to edge services and resiliency to loss of network connection is the major contribution of this work.

<img src="/assets/img/project/pscr/pic1_elastic_epc.jpg" width="100%">


<!---
## Emergency Message Broadcaster and Securing LTE Emergency Alerts

Modern cell phones are required to receive and display alerts via the Wireless Emergency Alert (WEA) program, under the
mandate of the Warning, Alert, and Response Act of 2006. These alerts include AMBER alerts, severe weather alerts, and
Presidential Alerts, intended to inform the public of imminent threats.
In our previous work, we showed the details of this system and developed and demonstrated the first practical spoofing attack on presidential alerts, using both commercially available hardware as well as modified open source software.

In this project, we will enhance this system to be an emergency message broadcaster such that it can effectively deliver
a text-based information to a large number of civilians without the cellular infrastructure. 
On the other hand, we propose to develop LEAST (Lightweight Emergency Alert Spoofing Tracker), a system that detects and localizes those attackers in real time, which can make significant contributions to U.S. national security by rapidly and accurately counteracting a wide range of cellular broadcast-based security attacks that can happen in the near future.
-->


## Offline Map Sharing

Our goal is to develop a framework that simplifies the production of complex mobile applications.
We develop a distributed spatial computing application that focuses on messaging,
image dissemination and map retrieval, which is inspired by [Serval project](http://servalproject.org). We 
implement optimized distributed spatial data organized that can be used to rapidly identify shared and
geo-spatially distributed representations of common map information.


<img src="/assets/img/project/pscr/pic3_map_sharing.jpeg" width="100%">


<!--
## Distributed Coordination for Massive Downloading

We presents a fully distributed scheduling framework called CASTLE (Client-side Adaptive Scheduler That minimizes Load
and Energy), which jointly optimizes the spectral efficiency of cellular networks and battery consumption of smart
devices. To do so, we focus on scenarios when many smart devices compete for cellular resources in the same base
station: spreading out transmissions over time so that only a few devices transmit at once improves both spectral
efficiency and battery consumption. To this end, we devise two novel features in CASTLE. First, we explicitly consider
inter-cell interference for accurate cellular load estimation. Based on our observations, we exploit the RSRQ (Reference
Signal Received Quality) and SINR as features in a machine learning algorithm to accurately estimate the cellular load.
Second, we propose a fully distributed scheduling algorithm that coordinates transmissions between clients based on the
locally estimated load level at each client. Our formulation for minimizing battery consumption at each device leads to
an optimized backoff-based algorithm that fits practical environments. To evaluate these features, we prototype a
complete LTE system testbed consisting of mobile devices, eNodeBs, EPC (Evolved Packet Core) and application servers.
Our comprehensive experimental results show that CASTLE’s load estimation is up to 91\% accurate, and that CASTLE
achieves higher spectral efficiency with less battery consumption, compared to existing centralized scheduling
algorithms as well as a distributed CSMA-like protocol. Furthermore, we develop a light-weight SDK that can expedite the
deployment of CASTLE into smart devices and evaluate it in a commercial LTE network.
-->


