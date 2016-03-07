---
title: collectd Kafka Plugin
brief: Kafka metrics for collectd.
---

# ![](https://github.com/signalfx/Integrations/blob/master/collectd-kafka/img/integrations_kafka.png) Kafka Plugin

- [Description](#description)
- [Requirements and Dependencies](#requirements-and-dependencies)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Metrics](#metrics)
- [License](#license)

### DESCRIPTION

This is the SignalFx Kafka plugin. Follow these instructions to configure the Java plugin for collectd to monitor Kafka. This will send data about Kafka to SignalFx, enabling built-in Kafka monitoring dashboards.

### REQUIREMENTS AND DEPENDENCIES

#### Version information

| Software          | Version        |
|-------------------|----------------|
| collectd          | 4.9 or later   |
| Elasticsearch     | 1.0.0 or later |

### INSTALLATION

1. Install the Java plugin.

 RHEL/CentOS 6.x & 7.x, and Amazon Linux 2014.09, 2015.03 & 2015.09

 Run the following command to install the Java plugin for collectd:

 ```
 yum install collectd-java
 ```
 Ubuntu 12.04, 14.04, 15.04 & Debian 7, 8:

 This plugin is included with [SignalFx's collectd package](https://github.com/signalfx/Integrations/tree/master/collectd).

1. Download SignalFx's sample JMX configuration file and sample Kafka configuration file from the following URLs:

 [JMX.conf](https://github.com/signalfx/Integrations/collectd-jmx/10-jmx.conf)
 [kafka-conf](https://github.com/signalfx/Integrations/collectd-kafka/20-kafka.conf)

 *Note: If you're using Kafka v0.8.2, download this sample Kafka configuration file instead:*
 [kafka.conf](https://github.com/signalfx/Integrations/collectd-kafka/20-kafka_82.conf)

1. Modify the configuration file providing values that make sense for your environment, as described [below](#configuration).

1. Add the following line to /etc/collectd.conf, replacing the example path with the location of the configuration file you downloaded in step 3:
 ```
 include '/path/to/10-jmx.conf'
  include '/path/to/20-kafka.conf'
 ```
or
 ```
 include '/path/to/10-jmx.conf'
  include '/path/to/20-kafka_82.conf'
 ```

1. Restart collectd.

collectd will begin emitting metrics from kafka.

### CONFIGURATION

* Make sure ServiceURL points to your jmx app.
* Modify the "Host" parameter to what you want your source name to be.
* Please leave the identifier [hostHasService=kafka] in the hostname.

### USAGE


### METRICS

For documentation of the metrics and dimensions emitted by this plugin, [click here](././docs).

### LICENSE

This plugin is released under the Apache 2.0 license. See LICENSE for more details.