# docker-multinode-elasticsearch-cluster
This sets up a 3-node docker elasticsearch cluster. Replace hostname1, hostname2, and hostname3 with the actual server hostnames in the docker-compose.yaml file.

Run docker stack deploy -c docker-compose.yaml --with-registry-auth elasticsearch to set up the cluster. 

login to one of the elastic-search container and do curl -X GET http://elastic-0:9200/_cluster/stats?pretty to check the cluster status

The same docker-compose.yaml file can be extended to a multi-node (more thann 3 nodes) server setup by extending elasticsearch services from elastic-3, elastic-4, and so on.
