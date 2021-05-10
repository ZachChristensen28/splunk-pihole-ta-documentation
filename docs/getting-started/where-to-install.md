# Where to Install

Splunk platform Instance type | Supported | Required | Actions required/ Comments
----------------------------- | --------- | -------- | --------------------------
Search Heads | Yes | Yes | Install this add-on to all search heads.
Indexers | Yes | Conditional | Not required if heavy forwarders are used to collect data. Required if using Universal or Light Forwarders.
Heavy Forwarders | Yes | Conditional | Required, if HFs are used to collect this data source.
Universal Forwarders | Yes | Not required | The add-on includes an inputs.conf file that is disabled by default. This can be used to create an input on the forwarder if enabled.

\* For more information, see Splunk's [documentation](https://docs.splunk.com/Documentation/AddOns/released/Overview/Installingadd-ons) on installing Add-ons.