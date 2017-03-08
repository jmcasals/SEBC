What is ubertask optimization?

Ubertask: certain 'small tasks' such as ==> 
"By default a job that has less than 10 mappers only and one reducer, and the input size is less than the size of one HDFS block is said to be small job. 
This small job hadoop will consider as Uber task. So the hadoop job will significantly run faster for 'small' jobs also."

-----------------------------------------------------------------------------

Where in CM is the Kerberos Security Realm value displayed?

Administration > Settings > Kerberos Security Realm field

-----------------------------------------------------------------------------

Which CDH service(s) host a property for enabling Kerberos authentication?

Any

-----------------------------------------------------------------------------

How do you upgrade the CM agents?

https://www.cloudera.com/documentation/enterprise/5-5-x/topics/cm_ag_upgrading_cm.html


----------------------------------------------------------------------------
Give the tsquery statement used to chart Hue's CPU utilization?

select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=$SERVICENAME

-----------------------------------------------------------------------------

Name all the roles that make up the Hive service

Hive Metastore Server
Gateway
HiveServer2
WebHCat Server 

-----------------------------------------------------------------------------

What steps must be completed before integrating Cloudera Manager with Kerberos?

Ensure you have secured communication between the Cloudera Manager Server and Agents before you enable Kerberos on your cluster. 
