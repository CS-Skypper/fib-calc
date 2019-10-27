# fib-calc
Fibonacci's constant index calculator
This project was built to practice using a multi-container docker deployment pipeline. On its surface, it is just a Fibonacci calculator. In order to determine and communicate the Fibonacci number for a given index, it uses the following services:
 - Node API server
 - Node worker service
 - Redis
 - Postgres
 - Nginx
 - React UI

It will be deployed to AWS Elastic Beanstalk using Travis CI and Dockerhub.

For development, I wrote a .travis.yml file that builds the docker images, runs tests, and pushes the images up to docker hub.

I used AWS Elastic Beanstalk multi-container deployment and wrote a Dockerrun.aws.json file that maps the containers in the docker-compose.yml to the AWS environment. The Dockerrun file pulls the images from Docker Hub so that I don't have to build them in the production enviroment.

I set up a Postgres service with AWS RDS.

I built this following Stephen Grider's Udemy tutorial on Docker and Kubernetes: https://www.udemy.com/docker-and-kubernetes-the-complete-guide
