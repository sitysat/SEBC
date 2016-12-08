# hive configuration
- sentry service = sentry
- HiveServer2 Enable Impersonation = false
# hue
- sentry service = sentry

connect beeline

!connect jdbc:hive2://ip-172-31-1-144.ap-southeast-1.compute.internal:10000/default;principal=hive/ip-172-31-1-144.ap-southeast-1.compute.internal@GBCHADOOP.COM