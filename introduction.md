#Introduction

NSX for vSphere allows the Distributed Firewall to enforce at the vNIC of every workload. This results in the ability to provide security boundaries at the point connectivity for a workload. Therefore it is crucial to understand the north/south traffic patterns in conjunction with east/west communications. The granular enforcement points means that security administrators need to protect at a new enforcement point.

The goal of this is book is to provide readers with the ability to use syslog to help segment any application. The approach discussed in this Day One book will allow administrators to:

* Benefits of centralised logs
* Understand the use of Distributed Firewall tags
* Utilising log functionality to collect traffic data
* Visualise log data in a syslog platform such as VMware Log Insight
* Leverage inbuilt functionality build policy for a single-tier and a multi-tier application
* Develop a repeatable process for all applications

The approach works for the following traffic patterns:
* Virtual to Physical communications
* Physical to Virtual communications
* Virtual to Virtual communications

It is quite apparent that given the virtaulised nature of NSX for vSphere physical to physical workloads cannot be captured. With that said any log data from physical devices can be utilised to build rules for physical to physical communication flows.

**note** Whilst this document uses VMware Log Insight the approach and methods (excluding Log Insight specifc queries and alerts) can be reproduce on LogStash/Grafana, Splunk, or other log and visualisation products.
