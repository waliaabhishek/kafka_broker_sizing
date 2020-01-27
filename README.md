# kafka_broker_sizing
This small excel sheet can be used to calculate minimum number of brokers required for minimum viable stable Kafka cluster.
It takes into account multiple requirements froma Kafka cluster perspective:

. Network Ingress and Egress requirement
. Disk throughput speeds
. Replication factor requirements
. Recommended broker soft limits

All the details are calculated on the basis of topic data requirement calculation which becomes the core strategy for cluster sizing.
