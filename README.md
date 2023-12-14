# docker-redis-server
redis server using docker

How to use?
Clone the project:
  $ git clone https://github.com/Minh-Quang-666/docker-redis-server.git
Start Redis via docker-compose in terminal:
  $ cd ./redis-docker-compose
  $ docker-compose up -d
Connect to the Redis server:
  $ docker exec -ti redis redis-cli -h 127.0.0.1 -p 6379 -a 12345678
Other commands maybe needed:
  # you can stop service by the command
  $ docker stop redis
  # you can start service by the command
  # maybe you need this command after your computer restart
  $ docker start redis
  # you can restart service by the command
  # maybe you need this command after you made some update for [redis.conf]
  $ docker restart redis
Q&A
How to change password?
Just change the line requirepass 12345678 in file redis.conf to requirepass [new password], and then restart the service with command docker restart redis