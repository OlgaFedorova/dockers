**Elasticserch**
_**Node-1**_

docker run --rm -d --net=host --env "ES_JAVA_OPTS=""-Xms512m -Xmx512m""" --ulimit memlock=-1:-1 -v /home/olga/dockers/elasticsearch/node1/logs:/usr/share/elasticsearch/logs -v /home/olga/dockers/elasticsearch/node1/data:/usr/share/elasticsearch/data -v /home/olga/dockers/elasticsearch/node1/config/elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml --name=elasticsearch1 docker.elastic.co/elasticsearch/elasticsearch:5.6.9 

**_Node-2_**

docker run --rm -d --net=host --env "ES_JAVA_OPTS=""-Xms512m -Xmx512m""" --ulimit memlock=-1:-1 -v /home/olga/dockers/elasticsearch/node2/logs:/usr/share/elasticsearch/logs -v /home/olga/dockers/elasticsearch/node2/data:/usr/share/elasticsearch/data -v /home/olga/dockers/elasticsearch/node2/config/elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml --name=elasticsearch2 docker.elastic.co/elasticsearch/elasticsearch:5.6.9 

**_Kibana_**

docker run --rm -d --net=host -v /home/olga/dockers/kibana/config/kibana.yml:/usr/share/kibana/config/kibana.yml --name=kibana docker.elastic.co/kibana/kibana:5.6.9

**_elasticsearch-curator-by-cron_**

docker run --rm -d --net=host -v /home/olga/dockers/elasticsearch-curator-by-cron/config:/usr/share/curator/config --name=elasticsearch-curator-by-cron elasticsearch-curator-by-cron:latest


