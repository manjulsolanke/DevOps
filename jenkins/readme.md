## Jenkins installation on Ubunut 22.04

### Installation steps on Ubunut 22.04

```bash
sudo apt update
sudo apt install default-jdk
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt update
sudo apt install jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
sudo ufw allow 8080
```

Note: tried and tested on ec2 Ubuntu 22.04


### Installation steps on docker

```bash
docker pull jenkins/jenkins:lts
docker run -p 8081:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts
```
