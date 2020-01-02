# Location Tracker api-gateway

## Make sure position-simulator, position-tracker, activemq and mongodb containers are running before api-gateway

## TEST APPLICATION 

1. Build Docker Image of api-gateway and push using following:   
docker push guptavinodkumar/lt-api-gateway:0.0.1-RELEASE

2. Create network (if not already created) --> docker network create locationtracker
   
3. RUN api gateway application:   
docker run -d --network locationtracker -p 8080:8080 --name apigateway --env position-tracker-url=http://positiontracker:8090 guptavinodkumar/lt-api-gateway:0.0.1-RELEASE



## SETTING UP GIT REPO
1.  git init
2. Go to Github and create repository lt-api-gateway
3. git remote add origin https://github.com/guptavinod/lt-api-gateway.git
4. git add .
5. git commit -m""
6. git push --set-upstream origin master
