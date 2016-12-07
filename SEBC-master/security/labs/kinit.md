Create a file kinit.md that includes:

- The kinit command you use to authenticate your test user
- The output from a klist command listing your credentials and ticket lifetime
```
[sitysat@ip-172-31-7-44 cloudera-scm-server]$ kinit
Password for sitysat@GBCHADOOP.COM:
[sitysat@ip-172-31-7-44 cloudera-scm-server]$ klist
Ticket cache: FILE:/tmp/krb5cc_501
Default principal: sitysat@GBCHADOOP.COM

Valid starting     Expires            Service principal
12/07/16 02:16:11  12/08/16 02:16:11  krbtgt/GBCHADOOP.COM@GBCHADOOP.COM
        renew until 12/14/16 02:16:11
```