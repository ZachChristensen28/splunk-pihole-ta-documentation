# Changelog

## Pi-hole Add-on for Splunk

### v1.3.0 <small>April 28, 2021</small>

* Added ability to pull regex and domain filters created in the Pi-hole server.
* Updated the Modular input to make more flexible.
* With the upcoming version of Pi-hole® 6.0, the scripted input "pihole_lists.sh" will be deprecated. This information will be available through the REST API in the upcoming release.

**Note**: This update changes the way the modular input works. If existing modular inputs were setup prior to this version, action must be taken to ensure those inputs continue to function correctly. See Updating to new modular inputs below or at https://github.com/ZachChristensen28/TA-pihole_dns/wiki/Updating-to-new-modular-Inputs.