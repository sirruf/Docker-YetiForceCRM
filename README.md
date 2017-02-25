
# YetiforceCRM 4.0.0 Docker

A Docker Compose environment which runs [YetiforceCRM](https://github.com/YetiForceCompany/YetiForceCRM/) in one container (php:7.1-apache)and a MySQL instance in another.	

### Running with Docker Compose

1. Install [Docker and Docker Compose](https://docs.docker.com/compose/install/)
2. Run `docker-compose up` from the root of this project.
3. Access `http://{docker_host}:8000` from your web browser to finish setting up YetiforceCRM.

### Running with Docker Run

If you already have MySQL installed or want to use a platform service like Amazon RDS, you can run the YetiforceCRM container seperately using Docker run. To set up YetiforceCRM using this approach, please do the following:

1. Install [Docker](http://docs.docker.com/installation/)
2. Run `docker run --name some-suitecrm -e DB_HOST_NAME=yourhostname -e DATABASE_NAME=yourdatabasename -e DB_USER_NAME=yourusername -e DB_PASSWORD=yourpassword -e DB_TYPE=mysql -e DB_TCP_PORT=3306 -e DB_MANAGER=MysqlManager -p 2080:80 -d spantree/suitecrm`
3. Access `http://{docker_host}:2080` from your web browser to finish setting up YetiforceCRM.