Elastic Beanstalk - Docker and Spring Boot
========================
Deploying Springboot Application to AWS Elastic Beanstalk from a Docker Container

Installation
--------------
* Clone this project
```sh
git clone https://github.com/adaofeliz/docker-springboot-ebs.git docker-springboot-ebs
```

* Build & Start Application
```sh
cd docker-springboot-ebs
mvn clean install
cd target/ebs_deploy/dist/
docker build -t docker-springboot-ebs .
docker run -p 8080:8080 docker-springboot-ebs
```

* Deploy with [EB Command Line Interface]
```sh
cd docker-springboot-ebs
mvn clean install
cd target/ebs_deploy/dist/
eb init # Follow Instructions
eb deploy
eb open
```

* Deploy Single File
```sh
cd docker-springboot-ebs
mvn clean install
# Use docker-springboot-ebs/target/ebs_deploy/elastic-beanstalk-docker.zip
```

Try it
--------------
- Open: http://localhost:8080/

License
--------------
MIT

[EB Command Line Interface]:http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-reference-eb.html
