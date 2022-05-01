# Blind Server Side Request Forgery (SSRF) in WP Ultimate CSV Importer

This PoC describe how to exploit a Blind SSRF in - WP Ultimate CSV Importer version 6.5.1

# Description

WP Ultimate CSV Importer v6.5.1 plugin for Wordpress does not have protections against SSRF, so it is possible to forge requests to internal services that are not directly exposed, if you know the path.

![1](https://user-images.githubusercontent.com/70114276/166161104-0a4a0cb6-9578-4fb2-8271-5c6a06ce045b.png)

## Attack Scenario

![2](https://user-images.githubusercontent.com/70114276/166161158-3fd88c6c-aa16-4a98-a12d-212ad2ee10d5.png)

After trying to directly access the service, we are not successful

![3](https://user-images.githubusercontent.com/70114276/166161168-81000a55-56f4-4eb5-ac5f-56b58d0dcd1e.png)

So we can perform a fake requests with this plugin through file upload by URL function

![8](https://user-images.githubusercontent.com/70114276/166161313-ed12212a-99d3-4941-8461-ffb51fc9b408.png)

![7](https://user-images.githubusercontent.com/70114276/166161250-89a304c4-d7e5-4893-bef7-d49a11b74cc0.png)

![6](https://user-images.githubusercontent.com/70114276/166161342-f313cf0c-b453-475d-8e94-d1df428f90ec.png)
