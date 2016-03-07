---
title: vmem collectd Plugin
brief: vmem (virtual memory) plugin for collectd.
---

![](https://github.com/signalfx/Integrations/blob/master/collectd/img/integrations_collectd.png)
# Example Python Plugin

- [Description](#description)
- [Requirements and Dependencies](#requirements-and-dependencies)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Metrics](#metrics)
- [License](#license)

### DESCRIPTION

From [collectd wiki]()
### REQUIREMENTS AND DEPENDENCIES

This plugin requires:

- collectd 4.4+

### INSTALLATION

This plugin is included with [SignalFx collectd](https://github.com/signalfx/Integrations/tree/master/collectd).

### CONFIGURATION

Configuration for this plugin is kept in the main [collectd.conf](https://github.com/signalfx/Integrations/blob/master/collectd/collectd.conf) file.

From the [collectd wiki](https://collectd.org/documentation/manpages/collectd.conf.5.shtml#plugin_vmem):

> The vmem plugin collects information about the usage of virtual memory. Since the statistics provided by the Linux kernel are very detailed, they are collected very detailed. However, to get all the details, you have to switch them on manually. Most people just want an overview over, such as the number of pages read from swap space.

| Configuration Option | Type | Definition |
|----------------------|------|------------|
|Verbose| true/false|Enables verbose collection of information. This will start collecting page "actions", e. g. page allocations, (de)activations, steals and so on. Part of these statistics are collected on a "per zone" basis.|

### USAGE

### METRICS

For documentation of the metrics and dimensions emitted by this plugin, [click here](././docs).

### LICENSE

License for this plugin can be found [in the header of the plugin](https://github.com/collectd/collectd/blob/master/src/vmem.c)