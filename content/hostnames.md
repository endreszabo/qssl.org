---
title: "Hostnames to reach your project"
date: 2019-10-15T09:00:00
draft: false
---

The certificate itself is a wildcard certificate that is valid for hosts matching `*.qssl.org`. Here comes the spooky part. You can already reach your site using a special subdomain under `qssl.org`. See [next chapter](#hostnames) to find out how to use these subdomains.

| the qssl subdomain | will return... |
|:---|:---|
| `https://46-101-138-239.qssl.org/` | ... a DNS `A` record that points to the specified dotted quad IP address that is separated with `-`. |
| `https://serene-example-4269_herokuapp_com.qssl.org/` | ... a DNS `CNAME` record that points to the specified hostname of `serene-example-4269.herokuapp.com`, where each underscore (`_`) character is being replaced with a dot (`.`).|
| `https://openbsd.qssl.org/` | ... a DNS `CNAME` record that points to `openbsd.org`. If a simple word is specified, the DNS server will substitude an .org domain |

If your hostname happens to already contain an underscore (`_`) you'd simply want to specify a double underscore (`__`) instead. A kind of escaping, so the DNS server will return a `_` instead of `.` for that part.

## Test domains to demonstrate the service

I've setup some test domains of my own for you to see how it works:

- https://46-101-138-239.qssl.org/ This very server running qssl.org as well.
- https://end\_re.qssl.org/ my blog running at [end.re](https://end.re/) is equipped with the wildcard certificate.
