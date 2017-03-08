

[root@ip-192-168-0-161 ec2-user]#  curl -u admin:admin 'http://localhost:7180/api/v1/clusters'
{
  "items" : [ {
    "name" : "josepmaria_casals",
    "version" : "CDH5"
  } ]


---------------------------------------------

[root@ip-192-168-0-161 ec2-user]# curl -u admin:admin   'http://localhost:7180/api/v1/clusters/josepmaria_casals/services'
{
  "items" : [ {
    "name" : "impala",
    "type" : "IMPALA",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/impala",
    "serviceState" : "STOPPED",
    "healthSummary" : "DISABLED",
    "healthChecks" : [ {
      "name" : "IMPALA_ASSIGNMENT_LOCALITY",
      "summary" : "DISABLED"
    }, {
      "name" : "IMPALA_CATALOGSERVER_HEALTH",
      "summary" : "DISABLED"
    }, {
      "name" : "IMPALA_IMPALADS_HEALTHY",
      "summary" : "DISABLED"
    }, {
      "name" : "IMPALA_STATESTORE_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStale" : false
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/yarn",
    "serviceState" : "STOPPED",
    "healthSummary" : "DISABLED",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "DISABLED"
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "DISABLED"
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "DISABLED"
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStale" : false
  }, {
    "name" : "spark_on_yarn",
    "type" : "SPARK_ON_YARN",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/spark_on_yarn",
    "serviceState" : "STOPPED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ ],
    "configStale" : false
  }, {
    "name" : "hbase",
    "type" : "HBASE",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hbase",
    "serviceState" : "STOPPED",
    "healthSummary" : "DISABLED",
    "healthChecks" : [ {
      "name" : "HBASE_MASTER_HEALTH",
      "summary" : "DISABLED"
    }, {
      "name" : "HBASE_REGION_SERVERS_HEALTHY",
      "summary" : "DISABLED"
    } ],
    "configStale" : false
  }, {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
    "serviceState" : "STOPPED",
    "healthSummary" : "DISABLED",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "DISABLED"
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "DISABLED"
    } ],
    "configStale" : false
  }, {
    "name" : "solr",
    "type" : "SOLR",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/solr",
    "serviceState" : "STOPPED",
    "healthSummary" : "DISABLED",
    "healthChecks" : [ {
      "name" : "SOLR_SOLR_SERVERS_HEALTHY",
      "summary" : "DISABLED"
    } ],
    "configStale" : false
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hdfs",
    "serviceState" : "STARTED",
    "healthSummary" : "BAD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "CONCERNING"
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_FAILOVER_CONTROLLERS_HEALTHY",
      "summary" : "BAD"
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "BAD"
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD"
    } ],
    "configStale" : false
  }, {
    "name" : "ks_indexer",
    "type" : "KS_INDEXER",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/ks_indexer",
    "serviceState" : "STOPPED",
    "healthSummary" : "DISABLED",
    "healthChecks" : [ {
      "name" : "KS_INDEXER_HBASE_INDEXERS_HEALTHY",
      "summary" : "DISABLED"
    } ],
    "configStale" : false
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/oozie",
    "serviceState" : "STOPPED",
    "healthSummary" : "DISABLED",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "DISABLED"
    } ],
    "configStale" : false
  }, {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/zookeeper",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStale" : false
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster3"
    },
    "serviceUrl" : "http://ip-192-168-0-161.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hue",
    "serviceState" : "STOPPED",
    "healthSummary" : "DISABLED",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "DISABLED"
    } ],
    "configStale" : false
  } ]

----------------------------------------------------------------------
[root@ip-192-168-0-161 ec2-user]# curl -X POST -u admin:admin 'http://localhost:7180/api/v1/clusters/josepmaria_casals/services/hive/commands/start'

{
  "id" : 668,
  "name" : "Start",
  "startTime" : "2017-03-08T10:15:27.960Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster3",
    "serviceName" : "hive"
  }
}

[root@ip-192-168-0-161 ec2-user]# curl -X POST -u admin:admin 'http://localhost:7180/api/v1/clusters/josepmaria_casals/services/hive/commands/stop'

{
  "id" : 672,
  "name" : "Stop",
  "startTime" : "2017-03-08T10:15:36.111Z",
  "endTime" : "2017-03-08T10:15:36.111Z",
  "active" : false,
  "success" : false,
  "resultMessage" : "At least one role must be started.",
  "serviceRef" : {
    "clusterName" : "cluster3",
    "serviceName" : "hive"
  }
}

//Again for getting the status
[root@ip-192-168-0-161 ec2-user]# curl -u admin:admin   'http://localhost:7180/api/v1/clusters/josepmaria_casals/services'



