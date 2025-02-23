# Monitoring

1. Prometheus is a datasource which performs the monitoring. We need metrics for monitoring. It uses Time Series Database. Metrics - (RAM, CPU, Website is reachable pr not etc.)
2. Time Series Data - Scrape very time (every 10 sec  etc.) -> Custom Database for storage of metrics -> PromQL is a query language which is executed get data.
3. Prometheus gets metrics from endpoints /metrics.
4. We have separate components called exporters -> collects the metrics and expose it to the endpoints.
5. Two commonly used exporters are -
 a. Node exporter - scrape metrics from node / server / VM (CPU usage, RAM usage, Disc usage etc.)

   - > Installed on Worker Node 

   - > Port : 9100

 b. Blackbox exporter - Website is up or not, SSL is there or not

     - > can be installed anywhere (request is sent to website for information.



********Grafana******       

1. Grafana is a visualization tool which takes metrics from Prometheus and represent it in the form of  Tables, Charts, Graphs etc.


*Launch 2 EC2 -

1. EC2 1 - Deploy the website and install Node exporter.
2. EC2 2  - Install Prometheus, Grafana and Blackbox exporter.
*Edit prometheus.yml file to add the source for metrics.

*Add datasource as url of Prometheus in Grafana.







