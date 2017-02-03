# Docker-ELK-Stack
Elasticsearch, Logstash, Kibana logging stack for Docker using Docker Compose


After launching stack, test by launching a service with options:

--network <STACK_NAME>_logging --log-driver syslog --log-opt syslog-address=tcp://localhost:5000 --log-opt tag="<APPLICATION_NAME>/{{.Name}}"
