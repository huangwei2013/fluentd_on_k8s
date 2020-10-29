### es安装


* es单节点docker安装
使用的是es7.6.2版本(注：es7.x较之前版本有较大变化)
```
docker run -d --restart always -p 9200:9200 -p 9300:9300 -m 2048m -v /etc/elasticsearch/elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml --name elasticsearch -e "discovery.type=single-node" -e ES_JAVA_OPTS="-Xms1024m -Xmx2048m" elasticsearch:7.6.2

```


* elasticsearch-head 工具安装
提供一个es管理界面，实用
```
docker run -d --restart always --name head --link elasticsearch -p 9001:9100 docker.io/mobz/elasticsearch-head:5

```

安装后通过 http://安装的服务器IP:9001/ 访问
