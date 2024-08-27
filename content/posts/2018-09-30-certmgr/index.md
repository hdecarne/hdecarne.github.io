---
title: "Can't remember that openssl command line"
summary: "Tired from looking up the monstrous openssl docs everytime I had to handle one of my certificates, I decided to make my life easier. The result is the Certificate Manager tool ..."
date: 2018-09-30
draft: false
tags: ["certmgr", "Certificate Management"]
---
Tired from looking up the monstrous openssl docs everytime I had to handle one of my certificates, I decided to make my life easier.
The result is the Certificate Manager tool available for [download](https://github.com/hdecarne/certmgr/releases) here.

Using Certificate Manager you can:
 * Create and manage your **private certificates** (signed by your own Certificate Authority)
 * Create and manage your **public certificates** (signed by an external Certificate Authority)
 * Create and manage your **Certificate Revocation Lists** (CRLs)
 * **Import and export** certificates from various formats (PEM, DER, PKCS#12, JKS format) as well as from various sources (file, folder, url, server)

See the [Certificate Manager](https://certmgr.carne.de) home page for a complete description of the tool as well as HowTos for:
 * [Creating your own private CA](https://certmgr.carne.de/howtoLocalCA/)
 * [Creating and managing certificates of an external CA](https://certmgr.carne.de/howtoExternalCA/)
 * [Importing existing certificate objects](https://certmgr.carne.de/howtoImport/)
 * [Configuring Apache to use your certificates](https://certmgr.carne.de/howtoApache/).
