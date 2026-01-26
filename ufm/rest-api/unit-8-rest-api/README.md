# Unit 8 - REST API

how to get UFM toc ommunicate to external software?

to build integration&#x20;



eg. kubernetes plugin, slurm, openstack plugin

interacts with UFM rest API



Data Collection

REST API provides 2 main URL

```
/ufmRest/app/ ## data about app notifications
-> Events, Alarms, Logs, ...

/ufmRest/Resources/ ## data about managed elements in the fabrics
eg. Ports, Links, System cables, Groups, Servers, ...

```

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



Recommended integration



1. Colelct Events
2. Phrase Events
3. Check event version to detect new events in UFM



1 more function - Cluster health validation

GET /ufmRest/FabricValidation/tests/CheckSubnetManager

GET /ufmRest/jobs/job-id/info





