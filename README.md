# Docker-Registry-using-Amazon-ECS

#Create repository through command line

aws ecr create-repository --repository-name docker-ecr-repo --region eu-central-1

#To check description of repositories

aws ecr describe-repositories --region eu-central-1 

#Steps to make a dockerfile 
1. mkdir ecr
2. cd ecr
3. vi Dockerfile
4. Add commands from Dockerfile.txt

#Build the image

docker build -t docker-ecr-repo .

#to check image is successfully build

docker run docker-ecr-repo

#To push the repository in aws ecr

(aws ecr get-login --no-include-email --region eu-central-1)

#To tag the image of your ecr registry

docker tag imageid 948771985339.dkr.ecr.us-east-1.amazonaws.com/docker-ecr-repo:Latest

#To push the image into ecr

docker push 948771985339.dkr.ecr.us-east-1.amazonaws.com/

#Now you can check by pasting the ip in your webbrowser.


 
