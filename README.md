# elk3node-8.1.3
 三节点elk



控制台进入es01
./bin/elasticsearch-certutil ca
./bin/elasticsearch-certutil cert --ca elastic-stack-ca.p12


docker cp  1d1b79e6d0d9:/usr/share/elasticsearch/elastic-certificates.p12 elastic-certificates.p12


chmod -R 777 elastic-certificates.p12
