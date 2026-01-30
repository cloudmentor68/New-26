
## Install jenkins on ubuntu

```
sudo apt update
sudo apt install fontconfig openjdk-21-jre -y
java -version
```



```
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key
echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt update
sudo apt install jenkins -y
jenkins --version
```

Login to Jenkins using the below URL :- EX- `http://(ec2-instance-public-ip-address):8080`

  

```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
   

Click on Install suggested plugins





## Install Docker

```
sudo apt install docker.io -y
docker --version
```

```
sudo usermod -aG docker jenkins
```

```
sudo systemctl restart jenkins
```

## Start nodeapp project
