# GrafphD

GrafphD is a Docker implementation of StatsD, Graphite and Grafana. These are spread across two services. StatsD and Graphite on one, and Grafana on the other.

Launch the box with `docker-compose up`

Then you should be able to access the following URLs:

 - http://localhost:3000 - Grafana
 - http://localhost:5000 - Graphite
 
For the uninitiated, Graphite is the storage engine for Metrics, and Grafana is a powerful graphing interface which is able to read from Graphite.

## Configuring Grafana

You can log into Grafana with the username and password combination: admin/admin

From here, you can configure a Data Source to read from Graphite.

 - `Type` - Graphite
 - `Url` - http://localhost:5000
 - `Access` - direct
 
Then click Save & Test.

## Graphite

You can log into Grafana with the username and password combination: root/root

## Collecting Stats

If you want to collect stats with StatsD from within your application, you can configure your StatsD client to send data using the following credentials:

 - StatsD Host: http://localhost
 - StatsD Port: 8126
