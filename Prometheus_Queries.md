#Queries

It's kind of tough getting started with this querying without as much of an introduction.

Here's what I came up with until now:

 1. show cpu usage (aggregated to one minute each, or filtered, not sure): `irate(container_cpu_usage_seconds_total[1m])`
