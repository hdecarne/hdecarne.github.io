---
title: "Using AWS/Route53 for DDNS"
summary: "AWS/Route53 provides a fully featured DNS service, suitable for Dynamic DNS setup, but not yet well supported by the usual DDNS clients. The ddns-updater tool closes this gap ..."
date: 2023-03-18
draft: false
tags: ["ddns-updater", "Route53", "AWS"]
---
[AWS/Route53](https://aws.amazon.com/route53/) provides a fully featured and configurable DNS service for a reasonable price.
This makes it good choice for your Dynamic DNS setup. However Route53 is not yet well supported by the usual DDNS clients.
The ddns-updater tool closes this gap.

ddns-updater is a command line tool to perform dynamic DNS (DDNS) updates. It provides various finder mechanisms to gather the
running host's ip addresses and update mechanisms for several DNS backends.

The following address detection mechanisms are supported:
* Interface based (examining the addresses of the running host's interfaces)
* UPnP based (querying the local network's router for the external IPv4 address)
* Web based (querying one or more web based services to determine the running host's ip addresses)

The following DNS backends are supported:
* AWS/Route53 (updating AWS/Route53 zone information)
* Web (invoking a web based service to update DNS)

See the [ddns-updater](https://ddns-updater.carne.de) home page for the full command line description.
