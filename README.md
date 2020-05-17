# Kafka Broker Count Calculator
So, you have started on your journey with Kafka and you know how much data you will probably be sending to Kafka. You are happy to start with a 3 node cluster as that seems to be the minimum and you hope that it will not bottleneck Kafka deployment - "Hope". 

To counter this hope , I have worked on a spreadsheet which helps you determine your choke points and understand how can you scale your kafka infrastructure to get the best out of your system. 

The spreadsheets are available in various formats -- Open Sheets & MS Excel. Choos one and get started. 

It can be used to calculate minimum number of brokers required for minimum viable stable Kafka cluster. It takes into account multiple requirements froma Kafka cluster perspective:

* Network Ingress and Egress requirement
* Disk throughput speeds
* Disk capacity requirements
* Replication factor requirements
* Recommended broker soft limits

All the details are calculated on the basis of topic data requirement calculation which becomes the core strategy for cluster sizing.

## How it works:

The worksheet is primarily divided into two parts:
* Infrastructure team's responsibility -- Cells D10 through D15 and Cells G10 & G11. 
* Application Team's responsibility -- $19:$27 ( new Column for every topic type. 

The Sheet has been segregated to help segregate the responsibility of the Kafka Infrastructure team  - who might be responsible for managing the infrastructure ; and the other half is the application team -- those who do understand what data their topics will have , how many topics they will have (so on and so forth). Comments are provided for all the Cells that need input from the teams to help you will a seamless start. 

The best part is that for a standard use case scenarios, you will be able to determine your kafka broker requirements precisely without "hoping" to have enough bandwidth available for expansion. 

The spreadsheet also calculates some other critical numbers from a cluster perspective like:
* Average Ingress into the cluster
* Peak Ingress in the cluster
* Average Egress from the cluster
* Peak Egress from the cluster
* Total number of partitions in the whole cluster
* Total Disk Capacity required 
* Total Disk Capacity required per broker


