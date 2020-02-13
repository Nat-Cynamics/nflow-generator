#Vocabulary 
TARGET_IP  = target IP where we want to send the relative netflow Package
TARGET_PORT = target PORT ...
MIN = the minimum of package sent by the nflow-generator
MAX = the max of package sent by the nflow-generator


#Launching the nflow-Generator
./nflow-generator -t TARGET_IP -p TARGET_PORT -m MIN -e MAX
./nflow-generator -t TARGET_IP -p TARGET_PORT -m MIN -e MAX

#BUILD IMAGE
docker build -t cynamics/netflow .docker run cynamics/netflow:latest -t TARGET_IP -p TARGET_PORT -m MIN -e MAX

#RUN IMAGE
docker run cynamics/netflow:latest -t 10.118.136.211 -p 8041 -m 1000 -e 10000