This playbook starts up a docker environment with

1 ZooKeeper
2 Individual Kafka Brokers (kafka-source:9091 and kafka-target:9092)
2 Individual Schema Registries (http://schema-registry-source:8091 and http://schema-registry-target:8092)
1 Connect instance using kafka-target as its backing Kafka broker

In this config the two schema registries are running as a cluster.  It uses kafka-source as the backing broker.  Instance schema-registry-target has master.eligibility set to false meaning it won't be elected as master node.

