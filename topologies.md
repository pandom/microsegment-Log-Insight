# The topologies

The examples used throughout the book will refer to these two applications. There are two applications that will be subject to segmentation for this book. The first is a VMware Log Insight cluster and it represents a single-tier application. The second is the 'Bookstore' application and it represents a three-tier application. 

These topologies will be used for all examples throughout the book.

## VMware Log Insight

VMware Log Insight is a single tiered application. It is comprised of:

* 3 x Log Insight nodes

| Node | IP | Detail |
| -- | -- | -- |
| log | 192.168.100.80 | Log Insight VIP |
| log1 | 192.168.100.81 | Log Insight node 1 |
| log2 | 192.168.100.82 | Log Insight node 2 |
| log3 | 192.168.100.83 | Log Insight node 3 |

Below is an image of the logical topology.

![Log Insight topology](images/li-topology.png)

It provides the following network function for the application:

* Load Balancing via LVS

This application topology will demonstrate using Log Insight to define the rules to microsegment Log Insight itself.



## The 'Bookstore' application

The bookstore application is a commond three tier app. It is comprised of:

* 2 x Web VMs

* 2 x App VMs

* 1 x DB VM

| Node | IP | Detail |
| -- | -- | -- |
| web1 | 10.0.1.11 | Web VM |
| web2 | 10.0.1.12 | Web VM |
| app1 | 10.0.2.11 | App VM |
| app2 | 10.0.2.12 | App VM |
| db1 | 10.0.3.11 | DB VM |
| web VIP | 192.168.100.85 | NSX Edge VIP |
| app VIP | 172.16.0.6 | NSX Edge VIP |

Below is the image of the logical topology.

![Bookstore topology](images/bookstore-topology.png)

It has the following network requirements that are provided by VMware NSX

* Load Balancing for Web Tier
* Load Balancing for App Tier

This application topology will demonstrate using Log Insight to define the rules to microsegment common application stacks.
