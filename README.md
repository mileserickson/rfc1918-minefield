# Introduction

RFC1918 is a minefield. This is your map.

## RFC1918: Address Allocation for Private Internets

[RFC1918](https://tools.ietf.org/html/rfc1918) is an internet standard that designates certain ranges of IPv4 addresses for use in private networks:

* *10.0.0.0/8*
* *172.x.0.0/16*  (x must be between 16 and 31, inclusive)
* *192.168.x.0/24*  (x must be between 0 and 255, inclusive)

### Freedom

All of these address ranges are not routable on the internet. Because they are meant to be used internally on private networks, they can be used freely and without reservation.

### Caveat

Sometimes, users and administrators need to connect from one private network to another using a [VPN](https://en.wikipedia.org/wiki/Virtual_private_network). This becomes impossible if the two private networks have identical or overlapping subnets.

## The Mines: Ranges to Avoid

| Subnet              | Start            | End             | Reason                                   |
| ------------------- | ---------------- | --------------- | ---------------------------------------- |
| 10.0.0.0/24         | 10.0.0.0         | 10.0.0.255      | Commonly used                            |
| 10.1.1.0/24         | 10.1.1.0         | 10.1.1.255      | Commonly used                            |
| 10.10.1.0/24        | 10.10.1.0        | 10.10.1.255     | Default network (Asus)                   |
| 10.1.10.0/24        | 10.1.10.0        | 10.1.10.255     | Default network (Comcast)                |
| 172.16.0.0/24       | 172.16.0.0       | 172.16.0.255    | Commonly used                            |
| 172.17.0.0/16       | 172.17.0.0       | 172.17.255.255  | Kubernetes                               |
| 172.20.10.0/28      | 172.20.10.0      | 172.20.10.15    | Apple iPhone/iPad Personal Hotspots      |
| 192.168.0.0/24      | 192.168.0.0      | 192.168.0.255   | Default network (Linksys, Huawei)        |
| 192.168.1.0/24      | 192.168.1.0      | 192.168.1.255   | Default network (Linksys, Huawei)        |
| 192.168.2.0/24      | 192.168.2.0      | 192.168.2.255   | Default network (Linksys)                |
| 192.168.3.0/24      | 192.168.3.0      | 192.168.3.255   | Default network (Linksys, Huawei)        |
| 192.168.4.0/24      | 192.168.4.0      | 192.168.4.255   | Default network (Zoom, ZyXEL)            |
| 192.168.8.0/24      | 192.168.8.0      | 192.168.8.255   | Default network (Huawei)                 |
| 192.168.15.0/24     | 192.168.15.0     | 192.168.15.255  | Default network (Linksys)                |
| 192.168.16.0/24     | 192.168.16.0     | 192.168.16.255  | Default network (Linksys)                |
| 192.168.123.0/24    | 192.168.123.0    | 192.168.123.255 | Default network (Sitecom)                |
| 192.168.168.0/24    | 192.168.168.0    | 192.168.168.255 | Default network (SonicWall)              |
| 192.168.223.0/24    | 192.168.223.0    | 192.168.223.255 | Default network (Trendnet)               |
| 192.168.254.0/24    | 192.168.254.0    | 192.168.254.255 | Default network (Siemens, Actiontec)     |
