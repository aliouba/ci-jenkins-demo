# ci-jenkins-demo

mkdir ~/jenkins

cd ~/jenkins

docker pull jenkins/jenkins:lts

docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v $(pwd):/var/jenkins_home --restart always jenkins/jenkins:lts
