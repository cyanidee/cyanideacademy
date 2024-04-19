# Censys Search

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Picture of Censys Search</p></figcaption></figure>

Censys Search is a powerful tool to search for IPs behind WAFs (Web Application Firewall) such as for example CloudFlare. If you are lucky you can use different searching queries and a bit of your brain to try to connect the dots and you might be able to find the origin IP of the webserver that is behind the domain

#### How to Use Censys Search to find Origin IPs Behind WAFs

Censys Search has a big database of IPs and uses certificates (SSL) that can be linked from an possible origin IP to the domain.&#x20;

To discover origin IPs hidden Web Application Firewalls (WAFs) for example CloudFlare, you can follow the steps below to possibly find the origin IP. If&#x20;

1. **Start with basic search:** Search using basic information about the target. Always start with just entering the domain "example.com" directly in the search bar and then examine the results. You can go directly in each of the IPs you have found and try to connect to the ports that have HTTP.
2. **Use more pro haxxor queries:** You can use more advanced queries such as the one stated below. This query combined with your domain can narrow down your search and only find hosts that have HTTP services and which will more likely find you the origin IP on webservers.

```json
services: (port: 443 and service_name: HTTP)
```

3. **Look for certificate transparency logs:** Censys also indexes Certificate Transparency logs which can give u information aobut the domain's history and might reveal origin IPs that were registered before the WAF implementation. Use the `certificates` search with the domain name to uncover this data..



