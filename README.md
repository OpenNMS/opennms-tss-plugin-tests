# Timeseries Integration InMemory Plugin

This plugin exposes a simple implementation of the TimeSeriesStorage interface.
It holds the data in a Guava cache.
It can be used in OpenNMS to store and retrieve timeseries data.

This implementation ist meant to be a demonstration of how to implement the interface and for testing purposes.
It is not meant for production use.

## Usage
* compile: ``mvn install``
* activation: Enable the timeseries integration layer: TODO: Patrick add link once the documentation is online
* activate in Karaf shell: ``bundle:install -s mvn:org.opennms.plugins.timeseries.inmemory/timeseries-inmemory-plugin/1.0.0-SNAPSHOT``



