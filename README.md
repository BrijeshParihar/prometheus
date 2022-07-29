# Prometheus
prometheus is open-source system for monitor services and create alerts.prometheus hit the targets using http call in given interval to collect metrics and target service listen request on sepecified port number.it collect data and metrics from different services and store in timeshering database .prometheus uses PromQL query language to fetch data from timesharing database.
we can also monitor 3rd party software using expoter.

# dependency library for prometheus 
implementation 'org.springframework.boot:spring-boot-starter-actuator'

implementation 'io.micrometer:micrometer-registry-prometheus:1.8.3' 

# properties for prometheus in springboot project 
management:
  endpoints:
    web:
      cors:
        allowed-origins: '*'
        allowed-methods: OPTIONS,GET
        allowed-headers: '*'
      exposure:
        include: '*'
  metrics:
    distribution:
      percentiles-histogram:
        http:
          server:
            requests: true
 
# prometheus Default Port:
9090
# create docker image
docker build -t prometheus:latest .
# Create container
docker run -d -f 9090:9090 prometheus:latest
