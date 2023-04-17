# DCV Delegation for Partial Zones

## DNS > Record (CNAME Setup)

![](./1.CNAME DNS.png)


If you want to host a website name ```abc.jjonflare.cloud``` you need to create a partial Zone suffix in your authoritative DNS provider.

It will look like ```abc.jjonflare.cloud.cdn.cloudflare.net```

**Example on Godaddy DNS**

![](./2.partialdns.png)
![](./3.GodaddyDNS.png)


Next create CNAME record in your DNS provider for DCV delegation



**Example on Godaddy DNS**

_acme-challenge.abc abc.jjonflare.cloud.c43c00fbad46a7b5.dcv.cloudflare.com.

![](./4.DCV.png)

**On Cloudflare Dashboard**

Next add the CNAME record on Cloudflare dashboard ```abc.jjonflare.cloud```

![](./5.CloudflareDNS.png)

**Edge Certificate**

Navigate to SSL/TLS > Edge Certificate, order advanced certificate
For this example I selected **Google Trust Services** as Cloudflare will stop using **DigiCert** as an issuing certificate authority (CA) [More info here](https://developers.cloudflare.com/ssl/reference/migration-guides/digicert-update/advanced-certificates/)


![](./6.OrderAdvcert.png)
![](./7.googletrust.png)

And finally the certificate is issued on Cloudflare
![](./8.Certissued.png)
