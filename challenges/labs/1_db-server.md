[root@ip-172-31-23-60 ~]# hostname -f
ip-172-31-23-60.ap-southeast-1.compute.internal
[root@ip-172-31-23-60 ~]# mysql -uscm -pscm_password -e "status;"
--------------
mysql  Ver 15.1 Distrib 5.5.60-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          14
Current database:
Current user:           scm@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.60-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 4 min 42 sec

Threads: 1  Questions: 44  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.156
--------------

[root@ip-172-31-23-60 ~]# mysql -uscm -pscm_password -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| scm                |
+--------------------+
[root@ip-172-31-23-60 ~]# mysql -urman -prman_password -e "status;"
--------------
mysql  Ver 15.1 Distrib 5.5.60-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          16
Current database:
Current user:           rman@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.60-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 7 min 45 sec

Threads: 1  Questions: 51  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.109
--------------

[root@ip-172-31-23-60 ~]# mysql -urman -prman_password -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| rman               |
+--------------------+
[root@ip-172-31-23-60 ~]# mysql -uhive -phive_password -e "status;"
--------------
mysql  Ver 15.1 Distrib 5.5.60-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          19
Current database:
Current user:           hive@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.60-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 9 min 46 sec

Threads: 1  Questions: 58  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.098
--------------

[root@ip-172-31-23-60 ~]# mysql -uhive -phive_password -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| metastore          |
+--------------------+
[root@ip-172-31-23-60 ~]# mysql -uoozie -poozie_password -e "status;"
--------------
mysql  Ver 15.1 Distrib 5.5.60-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          23
Current database:
Current user:           oozie@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.60-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 12 min 58 sec

Threads: 1  Questions: 68  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.087
--------------

[root@ip-172-31-23-60 ~]# mysql -uoozie -poozie_password -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| oozie              |
+--------------------+
[root@ip-172-31-23-60 ~]# mysql -uhue -phue_password -e "status;"
--------------
mysql  Ver 15.1 Distrib 5.5.60-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          25
Current database:
Current user:           hue@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.60-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 14 min 30 sec

Threads: 1  Questions: 75  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.086
--------------

[root@ip-172-31-23-60 ~]# mysql -uhue -phue_password -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hue                |
+--------------------+
[root@ip-172-31-23-60 ~]# mysql -usentry -psentry_password -e "status;"
--------------
mysql  Ver 15.1 Distrib 5.5.60-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          27
Current database:
Current user:           sentry@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.60-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 14 min 59 sec

Threads: 1  Questions: 82  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.091
--------------

[root@ip-172-31-23-60 ~]# mysql -usentry -psentry_password -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| sentry             |
+--------------------+
