# Timeseries Storage Plugin Tests [![CircleCI](https://circleci.com/gh/OpenNMS/org.opennms.plugins.tss.plugin-tests.svg?style=svg)](https://circleci.com/gh/OpenNMS/org.opennms.plugins.tss.plugin-tests)

This repository contains tools to test Time Series Storage Plugins.

It also offers a simple in memory implementation of a time series storage plugin as reference and to try out the time series integration layer in opennms

## Tests
We have developed a set of test cases to check if a plugin implementation works properly.
In order to create a test for your plugin do the following:
* add a dependency to this jar:
  
  ```xml
  <dependency>
    <groupId>org.opennms.plugins.timeseries.inmemory</groupId>
    <artifactId>timeseries-inmemory-plugin</artifactId>
    <version>1.0.0-SNAPSHOT</version>
    <scope>test</scope>
  </dependency>
  ```
* extend `AbstractStorageIntegrationTest` like `InMemoryStorageTest` does.

For an example see: https://github.com/opennms-forge/timeseries-integration-influxdb

## In Memory Plugin
This plugin exposes a simple implementation of the TimeSeriesStorage interface.
It holds the data in a Guava cache.
It can be used in OpenNMS to store and retrieve timeseries data.

This implementation ist meant to be a demonstration of how to implement the interface and for testing purposes.
It is not meant for production use.

### Usage
* compile: ``mvn install``
* activation: Enable the timeseries integration layer: see [documentation](https://docs.opennms.org/opennms/releases/26.1.0/guide-admin/guide-admin.html#ga-opennms-operation-timeseries)
* activate in Karaf shell: ``bundle:install -s mvn:org.opennms.plugins.timeseries.inmemory/timeseries-inmemory-plugin/1.0.0-SNAPSHOT``

  
 



