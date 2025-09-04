# Jenkins Installation Process

Installing Jenkins on Ubuntu 24.04.3 LTS

1. Install OpenJDK
```bash
sudo apt install openjdk-21-jdk
```

2. Copy and Paste on your terminal
Documentation Link : https://www.jenkins.io/doc/book/installing/linux

```bash
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```
3. Check Jenkins Version

```bash
$ jenkins --version
2.516.2
```
4. Check Jenkins Service

```bash
$ sudo systemctl status jenkins
● jenkins.service - Jenkins Continuous Integration Server
     Loaded: loaded (/usr/lib/systemd/system/jenkins.service; enabled; preset: >
     Active: active (running) since Tue 2025-09-02 22:24:03 IST; 2min 35s ago
   Main PID: 10795 (java)
      Tasks: 45 (limit: 8953)
     Memory: 531.4M (peak: 578.7M)
        CPU: 33.490s
     CGroup: /system.slice/jenkins.service
```
5. Take initialPassword

```bash
$ sudo more /var/lib/jenkins/secrets/initialAdminPassword
e2992fd22dce4996a3d04e6bbb2962fa
```
6. Open Localhost

http://localhost:8080

7. Configure other Process

refere following video : https://www.youtube.com/watch?v=-wwOSWygXwU

