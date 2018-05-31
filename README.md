Elasticserch

docker run --rm -d --net=host -v /home/olga/dockers/elasticsearch/logs:/usr/share/elasticsearch/logs -v /home/olga/dockers/elasticsearch/data:/usr/share/elasticsearch/data -v /home/olga/dockers/elasticsearch/config/elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml --name=elasticsearch docker.elastic.co/elasticsearch/elasticsearch:5.6.9 

Kibana

docker run --rm -d --net=host -v /home/olga/dockers/kibana/config/kibana.yml:/usr/share/kibana/config/kibana.yml --name=kibana docker.elastic.co/kibana/kibana:5.6.9

elasticsearch-curator-by-cron

docker run --rm -d --net=host -v /home/olga/dockers/elasticsearch-curator-by-cron/config:/usr/share/curator/config --name=elasticsearch-curator-by-cron elasticsearch-curator-by-cron:latest

