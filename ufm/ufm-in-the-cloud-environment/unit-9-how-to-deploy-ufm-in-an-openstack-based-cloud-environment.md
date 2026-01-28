# Unit 9 - How to Deploy UFM in an OpenStack-Based Cloud Environment

UFM is key component of infiniband fabric and inifinabdn cloud



provide

* REST API
* CSP Allocation Systems
* Infra for Security
* Tenant isolation
* Tenant SLA



opencloud integration



steps

1. New Network POST Operation - `/ufmRest/cloudx/Network`
2. Add Port to existing network via POST operation `/ufmRest/cloudx/Port`



```
File: sm.conf
M key per port = true
File: partition.conf
Default Pkey, Ox7fff, all limited, self=FULL
```



once tenant created

Openstack ML2 Plugin sends notification to UFM REeST API

UFM Resume ... to bare metal resoures...

picky....

ML2 plugin interact with UFM Rest API

once tenant lifecycle, UFM receive naother notification from ML2 plugin



3 possible scnearios

1. Tenant A -> NodeInfo MAD -> Tenant B\
   block it&#x20;
2. Tenant B - run subnet manager in tenant node\
   UFM raised new event regard the blocking
3. Tenant A trying to send traffic to tenant B\
   switch blocks it - Bad P\_Key event



![](<../../.gitbook/assets/image (8) (1) (1) (1) (1) (1).png>)&#x20;





