# elk3node-8.1.3
 三节点elk



控制台进入es01
./bin/elasticsearch-certutil ca
./bin/elasticsearch-certutil cert --ca elastic-stack-ca.p12
elasticsearch-reset-password -u kibana_system -i
changeme

docker cp  1d1b79e6d0d9:/usr/share/elasticsearch/elastic-certificates.p12 elastic-certificates.p12


chmod -R 777 elastic-certificates.p12




#修改文件
sudo vim /etc/sysctl.conf
 
#添加参数
...
vm.max_map_count = 262144
1
2
3
4
5
6
重新加载/etc/sysctl.conf配置

sysctl -p



curl -XPUT -u elastic:changeme "http://10.0.2.11:9200/_license" -H "Content-Type: application/json" -d @jerry-young-863e135c-55d2-4257-b8c4-a031da3ca8d0-v5.json
