# Queries

It's kind of tough getting started with this querying without as much of an introduction.

Here's what I came up with until now:

 1. show cpu usage (aggregated to one minute each, or filtered, not sure): `irate(container_cpu_usage_seconds_total[1m])`
 1. cpu usage for each container: `sort_desc(sum(rate(container_cpu_user_seconds_total{image!=""}[1m])) by (name))`
 1. memory usage per container: `sort_desc(sum(container_memory_usage_bytes{image!=""}) by (name))`
 1. network usage per container: `sort_desc(sum by (name) (rate(container_network_receive_bytes_total{image!=""}[1m] ) ))`
