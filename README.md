# Docker-ELK-Stack
Elasticsearch, Logstash, Kibana logging stack for Docker using Docker Compose


After launching stack, test by launching a service with options:

Replace ALL_CAPS with your own values

--network STACK_NAME_logging --log-driver=syslog --log-opt syslog-address=tcp://IP_OF_HOST_IN_SWARM:5000 --log-opt tag="APPLICATION_NAME/{{.Name}}"


For example:

`docker deploy -c docker-compose-filter.yml elk_stack`

`docker service create --name es --network elk_stack_logging --log-driver=syslog --log-opt syslog-address=tcp://localhost:5000 --log-opt tag="ElasticSearch/{{.Name}}" elasticsearch`
