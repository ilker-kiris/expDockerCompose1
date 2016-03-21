### Exp project to migrate v1 docker-compose project to v2

# To run v1 docker-compose format;  
   cp docker-compose_v1.yml docker-compose.yml

# To run v2 docker-compose format;  
   cp docker-compose_v2.yml docker-compose.yml


## Example usage;
# To build image of web and start 3 containers (-d is for detached deamon mode)
   docker-compose up -d

 NOTE above builds an image expdockercompose1_web, 
      then starts 3 containers using images; jwilder/nginx-proxy, expdockercompose1_web, redis

      Afterwards you can hit it via below and it will return count of hits and the host name serving hit
  curl 0.0.0.0  
  
# To see containers running
   docker ps

# To see docker compose started containers running
   docker-compose ps

# To see logs while 3 containers are running
   docker-compose logs

# To increase number of web containers to 5
   docker-compose scale web=5

  then hit with curl and watch the logs, look how many web containers are running and returned host name to curl

# To decrease number of web containers to 2
   docker-compose scale web=2

 and watch the web containers reducing from 5 to 2 (watch via docker-compose ps) and in logs and in curl returned host name

# To stop them(all 3 containers above started)
   docker-compose down

