# Kinit command

In my home directory I create a keytab for my user and do this command

`kinit hadrien@SEBC.COM -k -t hadrien.keytab`

Here is the result for the klist command

```
[hadrien@manager ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_1001
Default principal: hadrien@SEBC.COM

Valid starting       Expires              Service principal
08/03/2017 14:33:26  09/03/2017 14:33:26  krbtgt/SEBC.COM@SEBC.COM
        renew until 15/03/2017 14:33:26
```
