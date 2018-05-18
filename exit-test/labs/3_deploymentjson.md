{
timestamp: "2018-05-18T04:44:48.949Z",
clusters: [
{
name: "cluster",
displayName: "vicngdeloitte",
version: "CDH5",
fullVersion: "5.11.2",
services: [
{
name: "hive",
type: "HIVE",
config: {
items: [
{
name: "hbase_service",
value: "hbase",
sensitive: false
},
{
name: "hive_metastore_database_host",
value: "ip-172-31-20-123.ap-southeast-1.compute.internal",
sensitive: false
},
{
name: "hive_metastore_database_password",
value: "hive_password",
sensitive: true
},
{
name: "mapreduce_yarn_service",
value: "yarn",
sensitive: false
},
{
name: "zookeeper_service",
value: "zookeeper",
sensitive: false
}
]
},
roles: [
{
name: "hive-GATEWAY-14843021e60c0e35da0b706f0bfa1b42",
type: "GATEWAY",
hostRef: {
hostId: "fb31ca5c-ad3c-4ae9-8edf-abcd3712b9f4"
},
config: {
items: [ ]
},
roleConfigGroupRef: {
roleConfigGroupName: "hive-GATEWAY-BASE"
}
},
{
name: "hive-GATEWAY-8ef2ab0758b8599d44b478356ca902ad",
type: "GATEWAY",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [ ]
},
roleConfigGroupRef: {
roleConfigGroupName: "hive-GATEWAY-BASE"
}
},
{
name: "hive-GATEWAY-9de6dfe5f1327e4a02c84c5bdc3bedfd",
type: "GATEWAY",
hostRef: {
hostId: "504eb6c1-b9a8-40f1-a122-dacc39c122f1"
},
config: {
items: [ ]
},
roleConfigGroupRef: {
roleConfigGroupName: "hive-GATEWAY-BASE"
}
},
{
name: "hive-GATEWAY-bf433fe00afd2c65d95ba53c79d2b14a",
type: "GATEWAY",
hostRef: {
hostId: "d78f4603-2224-4773-a197-bc49902e9989"
},
config: {
items: [ ]
},
roleConfigGroupRef: {
roleConfigGroupName: "hive-GATEWAY-BASE"
}
},
{
name: "hive-GATEWAY-f829c59550230b83994fa4d23f5f14a0",
type: "GATEWAY",
hostRef: {
hostId: "c1ad2091-3c96-400b-b734-d04647defc40"
},
config: {
items: [ ]
},
roleConfigGroupRef: {
roleConfigGroupName: "hive-GATEWAY-BASE"
}
},
{
name: "hive-HIVEMETASTORE-14843021e60c0e35da0b706f0bfa1b42",
type: "HIVEMETASTORE",
hostRef: {
hostId: "fb31ca5c-ad3c-4ae9-8edf-abcd3712b9f4"
},
config: {
items: [
{
name: "role_jceks_password",
value: "ci495l07g1f6sxfyfdjyt53de",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hive-HIVEMETASTORE-BASE"
}
},
{
name: "hive-HIVESERVER2-14843021e60c0e35da0b706f0bfa1b42",
type: "HIVESERVER2",
hostRef: {
hostId: "fb31ca5c-ad3c-4ae9-8edf-abcd3712b9f4"
},
config: {
items: [
{
name: "role_jceks_password",
value: "wrxvfwipbz2egc7fjqxb96en",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hive-HIVESERVER2-BASE"
}
}
],
displayName: "Hive",
roleConfigGroups: [
{
name: "hive-GATEWAY-BASE",
displayName: "Gateway Default Group",
roleType: "GATEWAY",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hive"
},
config: {
items: [ ]
}
},
{
name: "hive-HIVEMETASTORE-BASE",
displayName: "Hive Metastore Server Default Group",
roleType: "HIVEMETASTORE",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hive"
},
config: {
items: [
{
name: "hive_metastore_java_heapsize",
value: "1984954368",
sensitive: false
},
{
name: "hive_metastore_server_max_message_size",
value: "198495436",
sensitive: false
}
]
}
},
{
name: "hive-HIVESERVER2-BASE",
displayName: "HiveServer2 Default Group",
roleType: "HIVESERVER2",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hive"
},
config: {
items: [
{
name: "hiveserver2_java_heapsize",
value: "1984954368",
sensitive: false
},
{
name: "hiveserver2_spark_driver_memory",
value: "966367641",
sensitive: false
},
{
name: "hiveserver2_spark_executor_cores",
value: "4",
sensitive: false
},
{
name: "hiveserver2_spark_executor_memory",
value: "912680550",
sensitive: false
},
{
name: "hiveserver2_spark_yarn_driver_memory_overhead",
value: "102",
sensitive: false
},
{
name: "hiveserver2_spark_yarn_executor_memory_overhead",
value: "153",
sensitive: false
}
]
}
},
{
name: "hive-WEBHCAT-BASE",
displayName: "WebHCat Server Default Group",
roleType: "WEBHCAT",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hive"
},
config: {
items: [ ]
}
}
],
replicationSchedules: [ ]
},
{
name: "hbase",
type: "HBASE",
config: {
items: [
{
name: "hdfs_service",
value: "hdfs",
sensitive: false
},
{
name: "rm_dirty",
value: "true",
sensitive: false
},
{
name: "zookeeper_service",
value: "zookeeper",
sensitive: false
}
]
},
roles: [
{
name: "hbase-MASTER-8ef2ab0758b8599d44b478356ca902ad",
type: "MASTER",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "dr960anh45jd0fra6bybqw2ed",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hbase-MASTER-BASE"
}
},
{
name: "hbase-REGIONSERVER-8ef2ab0758b8599d44b478356ca902ad",
type: "REGIONSERVER",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "ctrz1ojuk3xayrkru7xp7xr0j",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hbase-REGIONSERVER-1"
}
},
{
name: "hbase-REGIONSERVER-9de6dfe5f1327e4a02c84c5bdc3bedfd",
type: "REGIONSERVER",
hostRef: {
hostId: "504eb6c1-b9a8-40f1-a122-dacc39c122f1"
},
config: {
items: [
{
name: "role_jceks_password",
value: "ddhtha2b7anr9y5a06ter2ea4",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hbase-REGIONSERVER-2"
}
},
{
name: "hbase-REGIONSERVER-bf433fe00afd2c65d95ba53c79d2b14a",
type: "REGIONSERVER",
hostRef: {
hostId: "d78f4603-2224-4773-a197-bc49902e9989"
},
config: {
items: [
{
name: "role_jceks_password",
value: "6tkqizqpwdqoysuhrigxdpnts",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hbase-REGIONSERVER-BASE"
}
},
{
name: "hbase-REGIONSERVER-f829c59550230b83994fa4d23f5f14a0",
type: "REGIONSERVER",
hostRef: {
hostId: "c1ad2091-3c96-400b-b734-d04647defc40"
},
config: {
items: [
{
name: "role_jceks_password",
value: "c25i9mdd9btdxshrpy4sof1e2",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hbase-REGIONSERVER-BASE"
}
}
],
displayName: "HBase",
roleConfigGroups: [
{
name: "hbase-GATEWAY-BASE",
displayName: "Gateway Default Group",
roleType: "GATEWAY",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hbase"
},
config: {
items: [ ]
}
},
{
name: "hbase-HBASERESTSERVER-BASE",
displayName: "HBase REST Server Default Group",
roleType: "HBASERESTSERVER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hbase"
},
config: {
items: [ ]
}
},
{
name: "hbase-HBASETHRIFTSERVER-BASE",
displayName: "HBase Thrift Server Default Group",
roleType: "HBASETHRIFTSERVER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hbase"
},
config: {
items: [ ]
}
},
{
name: "hbase-MASTER-BASE",
displayName: "Master Default Group",
roleType: "MASTER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hbase"
},
config: {
items: [
{
name: "hbase_master_java_heapsize",
value: "638582784",
sensitive: false
}
]
}
},
{
name: "hbase-REGIONSERVER-1",
displayName: "RegionServer Group 1",
roleType: "REGIONSERVER",
base: false,
serviceRef: {
clusterName: "cluster",
serviceName: "hbase"
},
config: {
items: [
{
name: "hbase_bucketcache_size",
value: "792",
sensitive: false
},
{
name: "hbase_regionserver_java_heapsize",
value: "638582784",
sensitive: false
}
]
}
},
{
name: "hbase-REGIONSERVER-2",
displayName: "RegionServer Group 2",
roleType: "REGIONSERVER",
base: false,
serviceRef: {
clusterName: "cluster",
serviceName: "hbase"
},
config: {
items: [
{
name: "hbase_regionserver_java_heapsize",
value: "1549795328",
sensitive: false
}
]
}
},
{
name: "hbase-REGIONSERVER-BASE",
displayName: "RegionServer Default Group",
roleType: "REGIONSERVER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hbase"
},
config: {
items: [
{
name: "hbase_regionserver_java_heapsize",
value: "2425356288",
sensitive: false
}
]
}
}
],
snapshotPolicies: [ ]
},
{
name: "zookeeper",
type: "ZOOKEEPER",
config: {
items: [ ]
},
roles: [
{
name: "zookeeper-SERVER-14843021e60c0e35da0b706f0bfa1b42",
type: "SERVER",
hostRef: {
hostId: "fb31ca5c-ad3c-4ae9-8edf-abcd3712b9f4"
},
config: {
items: [
{
name: "role_jceks_password",
value: "7r6m4bdlnpzutbvw4rtn0djpb",
sensitive: true
},
{
name: "serverId",
value: "1",
sensitive: false
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "zookeeper-SERVER-BASE"
}
},
{
name: "zookeeper-SERVER-8ef2ab0758b8599d44b478356ca902ad",
type: "SERVER",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "14xtlzgo8x49idq51p41xi3xv",
sensitive: true
},
{
name: "serverId",
value: "3",
sensitive: false
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "zookeeper-SERVER-BASE"
}
},
{
name: "zookeeper-SERVER-9de6dfe5f1327e4a02c84c5bdc3bedfd",
type: "SERVER",
hostRef: {
hostId: "504eb6c1-b9a8-40f1-a122-dacc39c122f1"
},
config: {
items: [
{
name: "role_jceks_password",
value: "2gqllwf7e2asmcl3f0qbmu6s",
sensitive: true
},
{
name: "serverId",
value: "2",
sensitive: false
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "zookeeper-SERVER-BASE"
}
}
],
displayName: "ZooKeeper",
roleConfigGroups: [
{
name: "zookeeper-SERVER-BASE",
displayName: "Server Default Group",
roleType: "SERVER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "zookeeper"
},
config: {
items: [
{
name: "maxSessionTimeout",
value: "60000",
sensitive: false
},
{
name: "zookeeper_server_java_heapsize",
value: "638582784",
sensitive: false
}
]
}
}
]
},
{
name: "hue",
type: "HUE",
config: {
items: [
{
name: "database_host",
value: "ip-172-31-20-123.ap-southeast-1.compute.internal",
sensitive: false
},
{
name: "database_password",
value: "hue_password",
sensitive: true
},
{
name: "database_type",
value: "mysql",
sensitive: false
},
{
name: "hbase_service",
value: "hbase",
sensitive: false
},
{
name: "hive_service",
value: "hive",
sensitive: false
},
{
name: "hue_webhdfs",
value: "hdfs-NAMENODE-14843021e60c0e35da0b706f0bfa1b42",
sensitive: false
},
{
name: "oozie_service",
value: "oozie",
sensitive: false
},
{
name: "zookeeper_service",
value: "zookeeper",
sensitive: false
}
]
},
roles: [
{
name: "hue-HUE_SERVER-8ef2ab0758b8599d44b478356ca902ad",
type: "HUE_SERVER",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "coyz01zesdfc1pst19ahpaaho",
sensitive: true
},
{
name: "secret_key",
value: "RElsCf02ug9OxKVhlgtkReUBU7E7KV",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hue-HUE_SERVER-BASE"
}
}
],
displayName: "Hue",
roleConfigGroups: [
{
name: "hue-HUE_LOAD_BALANCER-BASE",
displayName: "Load Balancer Default Group",
roleType: "HUE_LOAD_BALANCER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hue"
},
config: {
items: [ ]
}
},
{
name: "hue-HUE_SERVER-BASE",
displayName: "Hue Server Default Group",
roleType: "HUE_SERVER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hue"
},
config: {
items: [ ]
}
},
{
name: "hue-KT_RENEWER-BASE",
displayName: "Kerberos Ticket Renewer Default Group",
roleType: "KT_RENEWER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hue"
},
config: {
items: [ ]
}
}
]
},
{
name: "oozie",
type: "OOZIE",
config: {
items: [
{
name: "hive_service",
value: "hive",
sensitive: false
},
{
name: "mapreduce_yarn_service",
value: "yarn",
sensitive: false
},
{
name: "zookeeper_service",
value: "zookeeper",
sensitive: false
}
]
},
roles: [
{
name: "oozie-OOZIE_SERVER-8ef2ab0758b8599d44b478356ca902ad",
type: "OOZIE_SERVER",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "e7u5y3hzlok040mll3yg00ibl",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "oozie-OOZIE_SERVER-BASE"
}
}
],
displayName: "Oozie",
roleConfigGroups: [
{
name: "oozie-OOZIE_SERVER-BASE",
displayName: "Oozie Server Default Group",
roleType: "OOZIE_SERVER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "oozie"
},
config: {
items: [
{
name: "oozie_database_host",
value: "ip-172-31-20-123.ap-southeast-1.compute.internal",
sensitive: false
},
{
name: "oozie_database_password",
value: "oozie_password",
sensitive: true
},
{
name: "oozie_database_type",
value: "mysql",
sensitive: false
},
{
name: "oozie_database_user",
value: "oozie",
sensitive: false
},
{
name: "oozie_java_heapsize",
value: "638582784",
sensitive: false
}
]
}
}
]
},
{
name: "yarn",
type: "YARN",
config: {
items: [
{
name: "hdfs_service",
value: "hdfs",
sensitive: false
},
{
name: "rm_dirty",
value: "true",
sensitive: false
},
{
name: "zk_authorization_secret_key",
value: "EVu5BoOBjVVJBr95iVD4mKOvyCSjrD",
sensitive: true
},
{
name: "zookeeper_service",
value: "zookeeper",
sensitive: false
}
]
},
roles: [
{
name: "yarn-JOBHISTORY-14843021e60c0e35da0b706f0bfa1b42",
type: "JOBHISTORY",
hostRef: {
hostId: "fb31ca5c-ad3c-4ae9-8edf-abcd3712b9f4"
},
config: {
items: [
{
name: "role_jceks_password",
value: "6oo55z6l79h9sex5sf743fo6x",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "yarn-JOBHISTORY-BASE"
}
},
{
name: "yarn-NODEMANAGER-8ef2ab0758b8599d44b478356ca902ad",
type: "NODEMANAGER",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "2v5rvlf39cw84o1357jpd9o0n",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "yarn-NODEMANAGER-2"
}
},
{
name: "yarn-NODEMANAGER-9de6dfe5f1327e4a02c84c5bdc3bedfd",
type: "NODEMANAGER",
hostRef: {
hostId: "504eb6c1-b9a8-40f1-a122-dacc39c122f1"
},
config: {
items: [
{
name: "role_jceks_password",
value: "2bxlthyf7cb5y1rbc71p0cmms",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "yarn-NODEMANAGER-1"
}
},
{
name: "yarn-NODEMANAGER-bf433fe00afd2c65d95ba53c79d2b14a",
type: "NODEMANAGER",
hostRef: {
hostId: "d78f4603-2224-4773-a197-bc49902e9989"
},
config: {
items: [
{
name: "role_jceks_password",
value: "c46cfvpuo22eu38xu6mbn1yue",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "yarn-NODEMANAGER-BASE"
}
},
{
name: "yarn-NODEMANAGER-f829c59550230b83994fa4d23f5f14a0",
type: "NODEMANAGER",
hostRef: {
hostId: "c1ad2091-3c96-400b-b734-d04647defc40"
},
config: {
items: [
{
name: "role_jceks_password",
value: "bfpoek8eg0e9lqwqpt80k7n56",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "yarn-NODEMANAGER-BASE"
}
},
{
name: "yarn-RESOURCEMANAGER-14843021e60c0e35da0b706f0bfa1b42",
type: "RESOURCEMANAGER",
hostRef: {
hostId: "fb31ca5c-ad3c-4ae9-8edf-abcd3712b9f4"
},
config: {
items: [
{
name: "rm_id",
value: "63",
sensitive: false
},
{
name: "role_jceks_password",
value: "4330lr3v4ubys3fyt86oj9ew0",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "yarn-RESOURCEMANAGER-BASE"
}
}
],
displayName: "YARN (MR2 Included)",
roleConfigGroups: [
{
name: "yarn-GATEWAY-BASE",
displayName: "Gateway Default Group",
roleType: "GATEWAY",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "yarn"
},
config: {
items: [
{
name: "mapred_reduce_tasks",
value: "8",
sensitive: false
},
{
name: "mapred_submit_replication",
value: "2",
sensitive: false
}
]
}
},
{
name: "yarn-JOBHISTORY-BASE",
displayName: "JobHistory Server Default Group",
roleType: "JOBHISTORY",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "yarn"
},
config: {
items: [ ]
}
},
{
name: "yarn-NODEMANAGER-1",
displayName: "NodeManager Group 1",
roleType: "NODEMANAGER",
base: false,
serviceRef: {
clusterName: "cluster",
serviceName: "yarn"
},
config: {
items: [
{
name: "yarn_nodemanager_heartbeat_interval_ms",
value: "100",
sensitive: false
},
{
name: "yarn_nodemanager_local_dirs",
value: "/yarn/nm",
sensitive: false
},
{
name: "yarn_nodemanager_log_dirs",
value: "/yarn/container-logs",
sensitive: false
},
{
name: "yarn_nodemanager_resource_cpu_vcores",
value: "4",
sensitive: false
},
{
name: "yarn_nodemanager_resource_memory_mb",
value: "1922",
sensitive: false
}
]
}
},
{
name: "yarn-NODEMANAGER-2",
displayName: "NodeManager Group 2",
roleType: "NODEMANAGER",
base: false,
serviceRef: {
clusterName: "cluster",
serviceName: "yarn"
},
config: {
items: [
{
name: "node_manager_java_heapsize",
value: "638582784",
sensitive: false
},
{
name: "yarn_nodemanager_heartbeat_interval_ms",
value: "100",
sensitive: false
},
{
name: "yarn_nodemanager_local_dirs",
value: "/yarn/nm",
sensitive: false
},
{
name: "yarn_nodemanager_log_dirs",
value: "/yarn/container-logs",
sensitive: false
},
{
name: "yarn_nodemanager_resource_cpu_vcores",
value: "4",
sensitive: false
},
{
name: "yarn_nodemanager_resource_memory_mb",
value: "1024",
sensitive: false
}
]
}
},
{
name: "yarn-NODEMANAGER-BASE",
displayName: "NodeManager Default Group",
roleType: "NODEMANAGER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "yarn"
},
config: {
items: [
{
name: "yarn_nodemanager_heartbeat_interval_ms",
value: "100",
sensitive: false
},
{
name: "yarn_nodemanager_local_dirs",
value: "/yarn/nm",
sensitive: false
},
{
name: "yarn_nodemanager_log_dirs",
value: "/yarn/container-logs",
sensitive: false
},
{
name: "yarn_nodemanager_resource_cpu_vcores",
value: "4",
sensitive: false
},
{
name: "yarn_nodemanager_resource_memory_mb",
value: "3007",
sensitive: false
}
]
}
},
{
name: "yarn-RESOURCEMANAGER-BASE",
displayName: "ResourceManager Default Group",
roleType: "RESOURCEMANAGER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "yarn"
},
config: {
items: [
{
name: "yarn_scheduler_maximum_allocation_mb",
value: "3007",
sensitive: false
},
{
name: "yarn_scheduler_maximum_allocation_vcores",
value: "4",
sensitive: false
}
]
}
}
]
},
{
name: "hdfs",
type: "HDFS",
config: {
items: [
{
name: "dfs_ha_fencing_cloudera_manager_secret_key",
value: "F6FGvCl9HyXmpA7ljAnt9q2I6RAa4v",
sensitive: true
},
{
name: "fc_authorization_secret_key",
value: "CMWYXhf8L8cKaZTATHgAtCs4GMi0ED",
sensitive: true
},
{
name: "http_auth_signature_secret",
value: "DWMg5gGY6naTYNioh0Gs0bAScMCziN",
sensitive: true
},
{
name: "rm_dirty",
value: "true",
sensitive: false
},
{
name: "zookeeper_service",
value: "zookeeper",
sensitive: false
}
]
},
roles: [
{
name: "hdfs-BALANCER-14843021e60c0e35da0b706f0bfa1b42",
type: "BALANCER",
hostRef: {
hostId: "fb31ca5c-ad3c-4ae9-8edf-abcd3712b9f4"
},
config: {
items: [ ]
},
roleConfigGroupRef: {
roleConfigGroupName: "hdfs-BALANCER-BASE"
}
},
{
name: "hdfs-DATANODE-8ef2ab0758b8599d44b478356ca902ad",
type: "DATANODE",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "4vknj1aedyqr6rioglr0nm4od",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hdfs-DATANODE-1"
}
},
{
name: "hdfs-DATANODE-9de6dfe5f1327e4a02c84c5bdc3bedfd",
type: "DATANODE",
hostRef: {
hostId: "504eb6c1-b9a8-40f1-a122-dacc39c122f1"
},
config: {
items: [
{
name: "role_jceks_password",
value: "deacmmeebbmclowbaa84623jy",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hdfs-DATANODE-2"
}
},
{
name: "hdfs-DATANODE-bf433fe00afd2c65d95ba53c79d2b14a",
type: "DATANODE",
hostRef: {
hostId: "d78f4603-2224-4773-a197-bc49902e9989"
},
config: {
items: [
{
name: "role_jceks_password",
value: "2uqbp69qcr6ntaij6oq9dx403",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hdfs-DATANODE-BASE"
}
},
{
name: "hdfs-DATANODE-f829c59550230b83994fa4d23f5f14a0",
type: "DATANODE",
hostRef: {
hostId: "c1ad2091-3c96-400b-b734-d04647defc40"
},
config: {
items: [
{
name: "role_jceks_password",
value: "7sj5i7aqcmlakub4nx47go0ng",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hdfs-DATANODE-BASE"
}
},
{
name: "hdfs-NAMENODE-14843021e60c0e35da0b706f0bfa1b42",
type: "NAMENODE",
hostRef: {
hostId: "fb31ca5c-ad3c-4ae9-8edf-abcd3712b9f4"
},
config: {
items: [
{
name: "namenode_id",
value: "65",
sensitive: false
},
{
name: "role_jceks_password",
value: "4gisftaimkoblf126u7gbblvu",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hdfs-NAMENODE-BASE"
}
},
{
name: "hdfs-SECONDARYNAMENODE-9de6dfe5f1327e4a02c84c5bdc3bedfd",
type: "SECONDARYNAMENODE",
hostRef: {
hostId: "504eb6c1-b9a8-40f1-a122-dacc39c122f1"
},
config: {
items: [
{
name: "role_jceks_password",
value: "9nqqsmganqojg6ivj2p8dvhb5",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "hdfs-SECONDARYNAMENODE-BASE"
}
}
],
displayName: "HDFS",
roleConfigGroups: [
{
name: "hdfs-BALANCER-BASE",
displayName: "Balancer Default Group",
roleType: "BALANCER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [ ]
}
},
{
name: "hdfs-DATANODE-1",
displayName: "DataNode Group 1",
roleType: "DATANODE",
base: false,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [
{
name: "datanode_java_heapsize",
value: "638582784",
sensitive: false
},
{
name: "dfs_data_dir_list",
value: "/dfs/dn",
sensitive: false
},
{
name: "dfs_datanode_du_reserved",
value: "5367553638",
sensitive: false
},
{
name: "dfs_datanode_max_locked_memory",
value: "830472192",
sensitive: false
}
]
}
},
{
name: "hdfs-DATANODE-2",
displayName: "DataNode Group 2",
roleType: "DATANODE",
base: false,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [
{
name: "dfs_data_dir_list",
value: "/dfs/dn",
sensitive: false
},
{
name: "dfs_datanode_du_reserved",
value: "5367553638",
sensitive: false
},
{
name: "dfs_datanode_max_locked_memory",
value: "2015363072",
sensitive: false
}
]
}
},
{
name: "hdfs-DATANODE-BASE",
displayName: "DataNode Default Group",
roleType: "DATANODE",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [
{
name: "dfs_data_dir_list",
value: "/dfs/dn",
sensitive: false
},
{
name: "dfs_datanode_du_reserved",
value: "5367553638",
sensitive: false
},
{
name: "dfs_datanode_max_locked_memory",
value: "3153068032",
sensitive: false
}
]
}
},
{
name: "hdfs-FAILOVERCONTROLLER-BASE",
displayName: "Failover Controller Default Group",
roleType: "FAILOVERCONTROLLER",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [ ]
}
},
{
name: "hdfs-GATEWAY-BASE",
displayName: "Gateway Default Group",
roleType: "GATEWAY",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [
{
name: "dfs_client_use_trash",
value: "true",
sensitive: false
}
]
}
},
{
name: "hdfs-HTTPFS-BASE",
displayName: "HttpFS Default Group",
roleType: "HTTPFS",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [ ]
}
},
{
name: "hdfs-JOURNALNODE-BASE",
displayName: "JournalNode Default Group",
roleType: "JOURNALNODE",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [ ]
}
},
{
name: "hdfs-NAMENODE-BASE",
displayName: "NameNode Default Group",
roleType: "NAMENODE",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [
{
name: "dfs_name_dir_list",
value: "/dfs/nn",
sensitive: false
},
{
name: "dfs_namenode_servicerpc_address",
value: "8022",
sensitive: false
}
]
}
},
{
name: "hdfs-NFSGATEWAY-BASE",
displayName: "NFS Gateway Default Group",
roleType: "NFSGATEWAY",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [ ]
}
},
{
name: "hdfs-SECONDARYNAMENODE-BASE",
displayName: "SecondaryNameNode Default Group",
roleType: "SECONDARYNAMENODE",
base: true,
serviceRef: {
clusterName: "cluster",
serviceName: "hdfs"
},
config: {
items: [
{
name: "fs_checkpoint_dir_list",
value: "/dfs/snn",
sensitive: false
}
]
}
}
],
replicationSchedules: [ ],
snapshotPolicies: [ ]
}
],
parcels: [
{
product: "CDH",
version: "5.11.2-1.cdh5.11.2.p0.4",
stage: "DISTRIBUTED",
clusterRef: {
clusterName: "cluster"
}
},
{
product: "CDH",
version: "5.11.2-1.cdh5.11.2.p0.4",
stage: "ACTIVATED",
clusterRef: {
clusterName: "cluster"
}
}
]
}
],
hosts: [
{
hostId: "504eb6c1-b9a8-40f1-a122-dacc39c122f1",
ipAddress: "172.31.18.70",
hostname: "ip-172-31-18-70.ap-southeast-1.compute.internal",
rackId: "/default",
config: {
items: [ ]
}
},
{
hostId: "fb31ca5c-ad3c-4ae9-8edf-abcd3712b9f4",
ipAddress: "172.31.20.123",
hostname: "ip-172-31-20-123.ap-southeast-1.compute.internal",
rackId: "/default",
config: {
items: [ ]
}
},
{
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3",
ipAddress: "172.31.23.103",
hostname: "ip-172-31-23-103.ap-southeast-1.compute.internal",
rackId: "/default",
config: {
items: [ ]
}
},
{
hostId: "d78f4603-2224-4773-a197-bc49902e9989",
ipAddress: "172.31.28.166",
hostname: "ip-172-31-28-166.ap-southeast-1.compute.internal",
rackId: "/default",
config: {
items: [ ]
}
},
{
hostId: "c1ad2091-3c96-400b-b734-d04647defc40",
ipAddress: "172.31.30.62",
hostname: "ip-172-31-30-62.ap-southeast-1.compute.internal",
rackId: "/default",
config: {
items: [ ]
}
}
],
users: [
{
name: "__cloudera_internal_user__mgmt-EVENTSERVER-8ef2ab0758b8599d44b478356ca902ad",
roles: [
"ROLE_USER"
],
pwHash: "95a19ce919b365e61c39e622473eae8289d5e3e52a9ccd65e23dd62f6ff42a95",
pwSalt: -4024175185209348000,
pwLogin: true
},
{
name: "__cloudera_internal_user__mgmt-HOSTMONITOR-8ef2ab0758b8599d44b478356ca902ad",
roles: [
"ROLE_USER"
],
pwHash: "4f6e5066bcf967b22c3ac6282db259f282e28c159a35552cec64a83f19bc557f",
pwSalt: 477879811454724600,
pwLogin: true
},
{
name: "__cloudera_internal_user__mgmt-REPORTSMANAGER-8ef2ab0758b8599d44b478356ca902ad",
roles: [
"ROLE_USER"
],
pwHash: "fc6d5e35f7db55c271bea68cdc38cf324e6e203d20a56025dbf4131578f2e208",
pwSalt: -3436412164231526000,
pwLogin: true
},
{
name: "__cloudera_internal_user__mgmt-SERVICEMONITOR-8ef2ab0758b8599d44b478356ca902ad",
roles: [
"ROLE_USER"
],
pwHash: "ee4866f1de1e430e8c738b5fa7f668947aa9a3a5f3cc5bbfcffa2ee229ba53bc",
pwSalt: -4434587615338856400,
pwLogin: true
},
{
name: "admin",
roles: [
"ROLE_ADMIN"
],
pwHash: "d0ff88b53a7a159464ca529519dee6ba70ef3209880b68d15c3456e196661c69",
pwSalt: -891107226366220300,
pwLogin: true
}
],
versionInfo: {
version: "5.11.2",
buildUser: "jenkins",
buildTimestamp: "20170811-0014",
gitHash: "3c3ea33a12076fb83a8f11c4452c52fac685d01b",
snapshot: false
},
managementService: {
name: "mgmt",
type: "MGMT",
config: {
items: [ ]
},
roles: [
{
name: "mgmt-ALERTPUBLISHER-8ef2ab0758b8599d44b478356ca902ad",
type: "ALERTPUBLISHER",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "7x2iypm0dtw0xtrz2m4ur7jgj",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "mgmt-ALERTPUBLISHER-BASE"
}
},
{
name: "mgmt-EVENTSERVER-8ef2ab0758b8599d44b478356ca902ad",
type: "EVENTSERVER",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "cx1b79w9cafjbm305ad34glw2",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "mgmt-EVENTSERVER-BASE"
}
},
{
name: "mgmt-HOSTMONITOR-8ef2ab0758b8599d44b478356ca902ad",
type: "HOSTMONITOR",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "2308l0vpzcjrhqpobaa63htci",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "mgmt-HOSTMONITOR-BASE"
}
},
{
name: "mgmt-REPORTSMANAGER-8ef2ab0758b8599d44b478356ca902ad",
type: "REPORTSMANAGER",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "8dju3li5tf86f0olht3uzdbc6",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "mgmt-REPORTSMANAGER-BASE"
}
},
{
name: "mgmt-SERVICEMONITOR-8ef2ab0758b8599d44b478356ca902ad",
type: "SERVICEMONITOR",
hostRef: {
hostId: "7e9a9edf-c480-4b46-a1f3-cb95cd0dfdd3"
},
config: {
items: [
{
name: "role_jceks_password",
value: "1c70ibfq06bmh7smu4icp3crk",
sensitive: true
}
]
},
roleConfigGroupRef: {
roleConfigGroupName: "mgmt-SERVICEMONITOR-BASE"
}
}
],
displayName: "Cloudera Management Service",
roleConfigGroups: [
{
name: "mgmt-ACTIVITYMONITOR-BASE",
displayName: "Activity Monitor Default Group",
roleType: "ACTIVITYMONITOR",
base: true,
serviceRef: {
serviceName: "mgmt"
},
config: {
items: [ ]
}
},
{
name: "mgmt-ALERTPUBLISHER-BASE",
displayName: "Alert Publisher Default Group",
roleType: "ALERTPUBLISHER",
base: true,
serviceRef: {
serviceName: "mgmt"
},
config: {
items: [ ]
}
},
{
name: "mgmt-EVENTSERVER-BASE",
displayName: "Event Server Default Group",
roleType: "EVENTSERVER",
base: true,
serviceRef: {
serviceName: "mgmt"
},
config: {
items: [
{
name: "event_server_heapsize",
value: "638582784",
sensitive: false
}
]
}
},
{
name: "mgmt-HOSTMONITOR-BASE",
displayName: "Host Monitor Default Group",
roleType: "HOSTMONITOR",
base: true,
serviceRef: {
serviceName: "mgmt"
},
config: {
items: [
{
name: "firehose_heapsize",
value: "638582784",
sensitive: false
},
{
name: "firehose_non_java_memory_bytes",
value: "830472192",
sensitive: false
}
]
}
},
{
name: "mgmt-NAVIGATOR-BASE",
displayName: "Navigator Audit Server Default Group",
roleType: "NAVIGATOR",
base: true,
serviceRef: {
serviceName: "mgmt"
},
config: {
items: [ ]
}
},
{
name: "mgmt-NAVIGATORMETASERVER-BASE",
displayName: "Navigator Metadata Server Default Group",
roleType: "NAVIGATORMETASERVER",
base: true,
serviceRef: {
serviceName: "mgmt"
},
config: {
items: [ ]
}
},
{
name: "mgmt-REPORTSMANAGER-BASE",
displayName: "Reports Manager Default Group",
roleType: "REPORTSMANAGER",
base: true,
serviceRef: {
serviceName: "mgmt"
},
config: {
items: [
{
name: "headlamp_database_host",
value: "ip-172-31-20-123.ap-southeast-1.compute.internal",
sensitive: false
},
{
name: "headlamp_database_name",
value: "rman",
sensitive: false
},
{
name: "headlamp_database_password",
value: "rman_password",
sensitive: true
},
{
name: "headlamp_database_user",
value: "rman",
sensitive: false
},
{
name: "headlamp_heapsize",
value: "638582784",
sensitive: false
}
]
}
},
{
name: "mgmt-SERVICEMONITOR-BASE",
displayName: "Service Monitor Default Group",
roleType: "SERVICEMONITOR",
base: true,
serviceRef: {
serviceName: "mgmt"
},
config: {
items: [
{
name: "firehose_heapsize",
value: "638582784",
sensitive: false
},
{
name: "firehose_non_java_memory_bytes",
value: "830472192",
sensitive: false
}
]
}
},
{
name: "mgmt-TELEMETRYPUBLISHER-BASE",
displayName: "Telemetry Publisher Default Group",
roleType: "TELEMETRYPUBLISHER",
base: true,
serviceRef: {
serviceName: "mgmt"
},
config: {
items: [ ]
}
}
]
},
managerSettings: {
items: [
{
name: "CLUSTER_STATS_START",
value: "10/24/2012 17:30",
sensitive: false
},
{
name: "PUBLIC_CLOUD_STATUS",
value: "ON_PUBLIC_CLOUD",
sensitive: false
},
{
name: "REMOTE_PARCEL_REPO_URLS",
value: "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/",
sensitive: false
}
]
},
allHostsConfig: {
items: [ ]
},
peers: [ ],
hostTemplates: {
items: [ ]
}
}
