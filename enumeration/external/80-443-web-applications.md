---
description: Web applications run on port 80 (HTTP) and port 443 (HTTPS)
---

# 80/443 Web Applications

Web servers are a common target for hackers, because they can be used to get a foothold on the system (e.g. shell) or even an organisation's network. Scanning is usually detectable, but also can identify opportunities for further exploitation.

## Robots

Check the /robots.txt first before you do anything.

If the server denies you and says that "you're not a search engine", then change your user-agent in Burpsuite or Curl to be this:

```
"Mozilla/5.0 (compatible; bingbot/2.0 +http://www.bing.com/bingbot.htm)"
```

## Heartbleed vulnerability

Test web server:

```
sslscan $target.ip:443
```

## Shellshock

## Nikto

Test web app:

```
nikto -h $target.ip
```

## Dirb



## Dirbuster



## Gobuster

Enumerate directories of web app:

```
gobuster dir -e -w /usr/share/wordlists/dirb/common.txt -t 5 -u $target.url -q
```

## WordPress

WordPress is a popular website/blogging platform and is frequently targeted by hackers. Vulnerabilities are typically introduced through community-developed modules and themes. WPScan is a tool that scans for a variety of module/theme vulnerabilities and can also enumerate users.

### Update WPScan

```
wpscan --update
```

### Default scan

```
wpscan -u $target.url/wp
```

### Active enumeration

Scan time can be reduced by choosing specific options:

* \-p  Scans popular plugins only.
* \-vp  Scans vulnerable plugins only.
* \-ap  Scans all plugins.

The same options are available for WordPress themes:

### Enumerate users

```
wpscan -u $target.url --enumerate -u
```

One liner:

```
wpscan -u $target.url -e u,ap,at
```

### Nmap

Nmap has a WordPress script:

```
nmap -sV --script http-wordpress-enum $target.ip
```
