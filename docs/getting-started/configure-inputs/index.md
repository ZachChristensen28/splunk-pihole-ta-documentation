# Configure Splunk Input

**Objective**: Set the sourcetype to `pihole` in the inputs.conf file on the forwarder.

## Splunk Universal Forwarder Configuration

Download the latest [Splunk Universal Forwarder (UF)](https://www.splunk.com/en_us/download/universal-forwarder.html) appropriate for your server. _This UF should be installed on the same server as the Pi-Hole server_.

Install the UF according to [Splunk Docs](https://docs.splunk.com/Documentation/Forwarder/latest/Forwarder/Installtheuniversalforwardersoftware).

Once installed the configurations can be made. The following is a sample inputs.conf that can be pushed using a deployment server or configured on the UF itself. Place the following configurations in the `../local/inputs.conf` file.

```SHELL
# inputs.conf
[monitor:///var/log/pihole.log]
disabled = 0
sourcetype = pihole
# optionally specify an index, if configured.
# index = dns

[monitor:///var/log/pihole-FTL.log]
disabled = 0
sourcetype = pihole:ftl
# optionally specify an index, if configured.
# index = dns
```

**(Deprecated)** To enable the scripted input to allow mapping of blocked queries to the originating blocklists.

```SHELL
[script://./bin/pihole_lists.sh]
disabled = 0
sourcetype = pihole:lists
# Everyday at 4:01 AM
interval = 1 4 * * *
# optionally specify an index, if configured.
# index = dns
```

**Note:** The `interval` can be specified as a cron schedule or in seconds. It is recommended to use a cron schedule to avoid the script from executing on startup. For more information see Splunk's documentation for intervals in [inputs.conf](https://docs.splunk.com/Documentation/Splunk/latest/Admin/Inputsconf).

Push the configuration to the forwarder, if using a deployment server, or restart the UF if configuring on the UF itself.