# Prometheus
prometheus is open-source system for monitor services and create alerts.prometheus hit the targets using http call in given interval to collect metrics and target service listen request on sepecified port number.it collect data and metrics from different services and store in timeshering database .prometheus will PromQL query language to fetch data from timesharing database.
we can also monitor 3rd party software using expoter.
 
 
# prometheus Default Port:
9090
# create docker image
docker build -t prometheus:latest .
# Create container
docker run -d -f 9090:9090 prometheus:latest
