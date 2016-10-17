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
Then use `emerge --sync` to download latest Portage tree and bigdata-overlay. Emerge (-pv means "pretend", "verbose" options) Hadoop or any other package from the overlay and report issues.
```
# emerge -pv apache-hadoop-bin

These are the packages that would be merged, in order:

Calculating dependencies... done!
[ebuild  N     ] sys-cluster/apache-hadoop-bin-2.7.3::bigdata  209075 KiB

Total: 1 package (1 new), Size of downloads: 209075 KiB
```

# ToDo

Add `systemd` USE flag and relevant service definitions.
