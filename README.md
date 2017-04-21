# dashboards
Default Grafana dashboards for inspectIT

inspectIT provides a set of preconfigured dashboards that can be imported into a Grafana instance to visualize inspectIT data out of the box.

### Preconfigure Datasource in Grafana
The default dashboards provided on this page have been created with Grafana version 3.1.1. These dashboards may be incompatible with other Grafana versions.
To use the default dashboards, the data source must be configured correctly. Therefore follow these configuration steps

1. Enter the administration screen (Grafana icon)
2. Select Data Sources → Add new
3. Enter the following data:
  * Name: inspectit (use exactly this name to make the dashboards work out of the box)
  * Type: Choose InfluxDB
  * Default: Make this checked
  * URL: http://<INFLUX_HOST>:<INFLUX_HTTP_PORT>
  * Access: Choose proxy
  * Basic Auth: unselected
  * Database: inspectit 
  * User: inspectit
  * Password: password (or the password you set on the installation of the longterm database)

Make sure the data entered above is consistent with the configuration described in [Long-term Data Persistence Configuration](https://inspectit-performance.atlassian.net/wiki/display/DOC17/Long-term+Data+Persistence+Configuration). In particular, if you used other values for the database name, user, password, etc. then also configure Grafana respectively.
