# Monitoring Lab
### *What is ubertask optimization?*

An Uber Job occurs when multiple mapper and reducers are combined to use a single container. There are four core settings around the configuration of Uber Jobs found in the mapred-site.xml options presented in Table 9.3.

So Ubertask Optimization is the way to enable this mode to run single container for enough smalls jobs


### *Where in CM is the Kerberos Security Realm value displayed?*

This configuration can bbe found in the configuration page : Cloudera Manager > Administration > Settings > Security

### *Which CDH service(s) host a property for enabling Kerberos authentication?*

All 

### *How do you upgrade the CM agents?*


### *Give the tsquery statement used to chart Hue's CPU utilization?*

`select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=$SERVICENAME`

Founded in the chart builder of the chart "CPU Cores Used" in HUE page

### *Name all the roles that make up the Hive service*

There are services :
1. HiveServer2
2. Hive Metastore
3. Hive gateway
4. WebHCat server


### *What steps must be completed before integrating Cloudera Manager with Kerberos?*

There are four steps :
1. Have a working KDC (like MIT kerberos or Active Directory)
2. This KDC should be configure to have non-zero ticket lifetime and renewal lifetime
3. OpenLdap client libraries should be installed on the Cloudera Manager Server host if you want to use Active Directory. Also, Kerberos client libraries should be installed on ALL hosts.
4. Cloudera Manager needs an account that has permissions to create other accounts in the KDC.
