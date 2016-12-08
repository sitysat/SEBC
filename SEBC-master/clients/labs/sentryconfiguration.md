# hive configuration
- sentry service = sentry
- HiveServer2 Enable Impersonation = false
# hue
- sentry service = sentry

connect beeline

beeline> !connect jdbc:hive2://172.31.1.144:10000/default;principal=hive/ip-172-31-1-144.ap-southeast-1.compute.internal@GBCHADOOP.COM

####
# ln -s /usr/java/jdk1.7.0_75/bin/java /bin/java
# export HUE_CONF_DIR="/var/run/cloudera-scm-agent/process/`ls -1 /var/run/cloudera-scm-agent/process | grep HUE | sort -n | tail -1 `"
# getent group | grep hadoop
# HUE_IGNORE_PASSWORD_SCRIPT_ERRORS=1 HUE_DATABASE_PASSWORD=password ./hue useradmin_sync_with_unix