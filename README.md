# docker-compose-mongodb-replicaset
3 nodes mongodb replicaset via docker compose

# Use
1. add the following to /etc/hosts **It's very important for the client to connect to mongo1/2/3 perspectively.**
```
127.0.0.1       mongo1
127.0.0.1       mongo2
127.0.0.1       mongo3
```
2. run via bash
```
docker-compose up -d --wait
```
3. URI:
```
mongodb://127.0.0.1:27018,127.0.0.1:27019,127.0.0.1:27020/?replicaSet=rs0
# or
mongodb://mongo1:27018,mongo2:27019,mongo3:27020/?replicaSet=rs0
```
