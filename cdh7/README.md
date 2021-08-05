```shell
> cluster_setup.py --version=bquery://product=cm:version=7.4.3:released --manager=csa15-sec-1.vpc.cloudera.com \
  --database=postgresql --db-version=12 --java=DETERMINE_BY_CDH \
  --agents='bquery://product=cdh:version=7.1.7.0:official:L0_PASSED+parcels@csa15-sec-{11..20}.vpc.cloudera.com' \
  --include-service-types=HDFS,HBASE,HIVE_ON_TEZ,YARN,KAFKA,KUDU,STREAMS_MESSAGING_MANAGER,FLINK,SQL_STREAM_BUILDER,ATLAS,RANGER \
  --flink-version=bquery://product=csa:version=1.4.0.0:official \
  --save-template --use-kerberos --enable-auto-tls --no-locks \
  setup                                 # setup 1~10th nodes
  
> cluster_setup.py --version=bquery://product=cm:version=7.4.3:released --manager=csa15-sec-1.vpc.cloudera.com \
  --database=postgresql --db-version=12 --java=DETERMINE_BY_CDH \
  --agents='bquery://product=cdh:version=7.1.7.0:official:L0_PASSED+parcels@csa15-sec-{11..20}.vpc.cloudera.com' \
  --include-service-types=HDFS,HBASE,HIVE_ON_TEZ,YARN,KAFKA,KUDU,STREAMS_MESSAGING_MANAGER,FLINK,SQL_STREAM_BUILDER,ATLAS,RANGER \
  --flink-version=bquery://product=csa:version=1.4.0.0:official \
  --save-template --use-kerberos --enable-auto-tls --no-locks \
  --use-cm-to-add-agents add_cluster.   # setup 11~20th nodes with csa 1.4

> cluster_setup.py --version=bquery://product=cm:version=7.4.3:released --manager=csa15-sec-1.vpc.cloudera.com \
  --database=postgresql --db-version=12 --java=DETERMINE_BY_CDH \
  --agents='bquery://product=cdh:version=7.1.7.0:official:L0_PASSED+parcels@csa15-sec-{11..20}.vpc.cloudera.com' \
  --include-service-types=HDFS,HBASE,HIVE_ON_TEZ,YARN,KAFKA,KUDU,STREAMS_MESSAGING_MANAGER,FLINK,SQL_STREAM_BUILDER,ATLAS,RANGER \
  --flink-version=bquery://product=csa:version=1.4.0.0:official \
  --save-template --use-kerberos --enable-auto-tls --no-locks \
  --use-cm-to-add-agents upgrade_csa    # upgrade CSA parcel to 1.5
```
