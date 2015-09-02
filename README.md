# Dynatrace-User-Logins-Plugin
This plugin counts the number of client logins & provides two metrics: Successful Logins & Failed Logins and reports per username.

## Current Limitations

1) It won't count historical logins when it first runs, so to get data, setup the monitor then re-login to the client.
2) This must run on a collector installed locally to the server you wish to query.
3) Underlying metrics upon which this plugin relies are only updated when a user clicks login or test connection in client. Hence if a user logs into the client then leaves it open or logged in, there will be no new data generated. I suggest you use the metrics from this plugin in combination with the "Client socket connections" metric (from dynatrace client monitoring system profile) to get a true picture of currently connected users.

Find further information in the [dynaTrace community](https://community.dynatrace.com/community/display/DL/User+Logins+Plugin)
