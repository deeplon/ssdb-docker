# ssdb-docker
SSDB Dockerfile
#Install
docker pull leobuskin/ssdb-docker
Create Directory /docker/ssdb/conf  /docker/ssdb/data
Copy ssdb.conf to /docker/ssdb/conf

docker run -d -p 8888:8888 -v /docker/ssdb/conf/ssdb.conf:/ssdb/ssdb.conf -v /docker/ssdb/data:/ssdb/var --name ssdb leobuskin/ssdb-docker /ssdb/ssdb-server /ssdb/ssdb.conf
