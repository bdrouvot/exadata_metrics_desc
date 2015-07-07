Utility used to add the exadata metric description to the cellcli output on the fly

**Example:**

cellcli -e "list metriccurrent attributes metricObjectName,name,metricValue where name like 'DB.*' and metricObjectName='BDT'" | ./exadata_metrics_desc.pl

would produce something like:

```sh
 BDT   DB_FC_IO_RQ (Number of IO requests issued by a database to flash cache)                58,611 IO requests
 BDT   DB_FC_IO_RQ_SEC (Number of IO requests issued by a database to flash cache per second) 2.0 IO/sec
 .
 .
 .
```

Feel free to build the query you want on the metrics.
You just need to launch exadata_metrics_desc.pl to see the metric description being added on the fly
(as long as the metric name appears in the output of your initial query).
