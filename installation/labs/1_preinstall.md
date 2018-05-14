# System Configuration Checks
Currently there are 5 instances created:

SN | Instance ID
---|--------------------
1  | i-00a4306778a0a97bb
2  | i-0419d1b444f35630d
3  | i-05ac92dc9e2d591fd
4  | i-08354488aa58304d6
5  | i-0cdd0fd040de57507

1. Swappiness check for i-00a4306778a0a97bb

<img src="swappinesscheck1.png"/>


    After modifying swappiness and rebooting
<img src="swappinesscheck2.png"/>


2. Checking the mount attributes
<img src="mountattributes1.png"/>

4. Disable transparent hugepage by following the steps here
https://blacksaildivision.com/how-to-disable-transparent-huge-pages-on-centos

Checking the THP before modifying
<img src="thp1.png"/>

Checking the THP after rebooting
<img src="thp2.png"/>

5. Checking the network config
<img src="networkconfig.png"/>

6. nslookup and reverse nslookup
<img src="nslookup.png" />

7. nscd service
<img src="nscd.png" />

8. ntpd service
<img src="ntpd.png" />
