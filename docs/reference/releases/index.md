# Changelog

## Pi-hole Add-on for Splunk

### v1.3.1 <small>July 8, 2021</small>

* fixed issue causing internal logs to produce a checkpointer not defined error [#28](https://github.com/ZachChristensen28/TA-pihole_dns/issues/28)
* updated field extractions to include dnssec query events introduced in new Pi-Hole version (Core: v5.4, FTL v5.9).

### v1.3.0 <small>April 28, 2021</small>

* Added ability to pull regex and domain filters created in the Pi-hole server.
* Updated the Modular input to make more flexible.
* With the upcoming version of Pi-hole® 6.0, the scripted input "pihole_lists.sh" will be deprecated. This information will be available through the REST API in the upcoming release.

**Note**: This update changes the way the modular input works. If existing modular inputs were setup prior to this version, action must be taken to ensure those inputs continue to function correctly. See Updating to new modular inputs below or at https://github.com/ZachChristensen28/TA-pihole_dns/wiki/Updating-to-new-modular-Inputs.

### v1.2.8 <small>Feb 20, 2021</small>

* Added scripted input to ingest lists which enable the mapping of blocked queries to originating blocklists -> [#21](https://github.com/ZachChristensen28/TA-pihole_dns/issues/21)

### v1.2.7 <small>Dec 21, 2020</small>

* Added Modular Input for pulling select data from the HTTP API.

### v1.2.6 <small>Oct 18, 2020</small>

* Fixed Regex/Exact query blacklist events not being extracted -> Issue [#9](https://github.com/ZachChristensen28/TA-pihole_dns/issues/9)
* Fixed HTTPS record types fixed (type=65) -> Issue [#10](https://github.com/ZachChristensen28/TA-pihole_dns/issues/10)

### v1.2.5 <small>Sept 1, 2020</small>

* Added compatibility for DHCP events.
* New sourcetype: pihole:dhcp.
