# ansible-role-mongodb


inventory

```
[mongo-master]
10.3.1.23 mongodb_master=true

[mongo-replicas]
10.3.1.35
10.3.1.63

[mongo:children]
mongo-master
mongo-replicas

[mongo:vars]
mongodb_login_host = 10.3.1.23
mongo_bootstrap_servers='10.3.1.23:27017,10.3.1.35:27017,10.3.1.63:27017'
```
