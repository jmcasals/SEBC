root@ip-192-168-0-161 ec2-user]# curl -X GET -u "admin:admin" -i http://localhost:7180/api/v2/cm/deployment

..................


          "name" : "role_jceks_password",
          "value" : "9mxuqjoj3q9azeos8a5hm7mrx"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-5e6a8ecbed39b56b8c50aa7e29f3fd86",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "7f12d13a-9422-48e3-80c7-c75c63b05c5e"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "12e2f09y4o271bkfkgl811a03"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-5e6a8ecbed39b56b8c50aa7e29f3fd86",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "7f12d13a-9422-48e3-80c7-c75c63b05c5e"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "3tiu0wg3gz0jf7xef9kltxc8v"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/21/2012 6:40"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}[
