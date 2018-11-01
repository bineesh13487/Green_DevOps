This Github repo is  for 

1 : Nodejs for local development
2 : Jenkins declarative pipeline for multibranch code
3 : Nodejs application combined with haproxy for swarm setup

Details :

Info : We have a nodejs application running which displays message "hello world". Node code pulled from  "https://github.com/heroku/node-js-sample"

Steps :

## docker-compose.yml file is for localdevelopment, which will pick Dockerfile for build ##  

   Run docker compose up 

## jenkinsfile is for declarative pipeline script. This is 80% complete as intergration steps not included as i'm not completely familiar with node applications 
ntegration tests ##

## docker-stack.yml will deploy 3 replicas of nodejs combined with haproxy. This setup will pull the customised image which i created and is from my docker hub ##


   docker stack -c docker-stack.yml <stack name> --------> This will binb haproxy 80 to localhost 32760 . haproxy 80 will be redirects to nodejs app on port 5000

   Run curl -L localhost:32760 and hello-world message will be displayed . It may not displays the messages on browser due to the timeout settings i mentioned in haproxy config 
