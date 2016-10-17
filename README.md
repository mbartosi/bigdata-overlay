# bigdata-overlay
Big Data Gentoo overlay

# Installation using Portage modular sync system:

As user root create directory /usr/local/bigdata-overlay

Create file /etc/portage/repos.conf/bigdata-overlay.conf and paste:
```
[bigdata]
location = /usr/local/bigdata-overlay
sync-type = git
sync-uri = https://github.com/mbartosi/bigdata-overlay
auto-sync = Yes
```
