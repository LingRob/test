#h3 To create a Docker network, use the following command:
`docker network create <network-name>`


#h3 To run a MySQL Docker image named "db" with a root password of "my-secret-password", use the following command:
`docker run --name db -e MYSQL_ROOT_PASSWORD=my-secret-password -d mysql:latest`

#h3 To run the phpMyAdmin Docker image on the previously created network, use the following command:
`docker run --name myadmin -d --link db:db -p <port-number>:80 phpmyadmin/phpmyadmin`
