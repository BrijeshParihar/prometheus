# prometheus Default Port:
9090
# create docker image
docker build -t prometheus:latest .
# Create container
docker run -d -f 9090:9090 prometheus:latest
