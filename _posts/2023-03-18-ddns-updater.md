---
layout: post
title: Using AWS/Route53 for DDNS
---
### Quick view
[AWS/Route53](https://aws.amazon.com/route53/) provides a fully featured and configurable DNS service for a reasonable price.
This makes it good choice for your Dynamic DNS setup. However Route53 is not yet well supported by the usual DDNS clients.
The ddns-updater tool closes this gap.

<!--more-->

To use [AWS/Route53](https://aws.amazon.com/route53/) for your Dynamic DNS an AWS account is required. Furthermore a hosted zone has to
be setup in prior to using the ddns-updater tool (see Route53 documentation for how to do this). The ddns-updater tool is capable to update
the A (IPv4) and AAAA (IPv6) records in this hosted zone with your host's current IPv4 and/or IPv6 address.

For example, if the Route53 hosted zone is *mydomain.net* with configured A and AAAA records for the server name *myhost.mydomain.net* the command line

> java -jar ddns-updater-boot-<version\> --host myhost.mydomain.net

will determine the current IPv4 and IPv6 address of the current host and update the A and AAAA records if they differ.
Every 24h the update will be forced anyway to recover from undetected divergences. By applying the *--noipv4* or *--noipv6*
command line option the update can be restricted according to the actual host setup.

See the [ddns-updater](https://hdecarne-github.github.io/ddns-updater/) home page for the full command line description.
