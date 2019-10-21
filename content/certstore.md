
---
title: "Certificates that you can download for your projects"
date: 2019-10-15T10:00:00
draft: false
---

The certificate itself is a wildcard certificate that is valid for hosts matching `*.qssl.org`. Here comes the spooky part. You can already reach your site using a special subdomain under `qssl.org`. See [next chapter](#hostnames) to find out how to use these subdomains.

<a name="download"></a>

| download link | contains | password |
|:---|:---|:---|
| [PEM bundle](qssl.pem) | Base64 encoded certificate chain, bundled with private key | none |
| [PEM certchain](qssl-cert.pem) | Base64 encoded certificate chain only | none |
| [PEM key](qss-key.pem) | Base64 encoded private key | none |
| [DER end certificate](qssl.crt) | DER binary format end certificate | none |
| [DER intermediate certificate](qssl-le.crt) | DER binary format Let's Encrypt certificate | none |
| [DER private key](qssl.key) | DER binary format private key | none |
| [PKCS12 bundle](qssl.p12) | PKCS12 container with certificate chain and private key | `qssl` |

