# seminar_yaniv
first lab in YanivOMC Docker file _spring-music_java_alpin:slim

# add 2 network <felan><belan> to work 2gether
  docker build -t repo_ben/feapp:v1 .
  120  docker network create dblan
  121  docker network create felan
  122  docker network ls
  126  docker run -d --name db_mysql --network dblan -e MYSQL_ALLOW_EMPTY_PASSWORD=yes -e MYSQL_DATABASE=music yanivomc/spring-mysql:latest
  128  docker logs  -f db_mysql
  130  docker images
  132  docker run -itd  -p 8082:8080 --network dblan repo_ben/feapp:v2
  133  docker run -itd  -p 8082:8080 --network dblan repo_ben/feapp:v1
  140  docker network connect felan d313f868
  141  docker network connect felan c603d030

  
