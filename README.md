# ci-jenkins-demo

# Create docker registry

```
docker run -d -p 5000:5000 --restart always --name registry registry:2
```

# Compose Installation

```
sudo curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

# Pull the code
```
git clone https://github.com/aliouba/ci-jenkins-demo.git
cd ci-jenkins-demo
```

# Jenkins Installation
```
cd jenkins
docker pull jenkins
docker-compose up -d
```
