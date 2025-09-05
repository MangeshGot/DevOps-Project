
## Docker Installation Process

Installing Docker on Ubuntu 24.04.3 LTS

Link : https://docs.docker.com/engine/install/ubuntu

1. Copy and Paste on your terminal

```bash
  # Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
2. install docker packages
   ```bash
   $ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin 
   ```

3. Download Docker DEB Package and Install it
Link : https://docs.docker.com/desktop/setup/install/linux/ubuntu

Documentation Link : https://docs.docker.com/desktop/setup/install/linux/ubuntu 
Deb File Link : https://desktop.docker.com/linux/main/amd64/docker-desktop-amd64.deb?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-linux-amd64&_gl=1*com1wc*_ga*MTcyNzk3NDY2NC4xNzU2ODI2OTI5*_ga_XJWPQMJYHQ*czE3NTY4MzA3NDQkbzIkZzEkdDE3NTY4MzE0NDIkajUyJGwwJGgw

```bash
sudo apt-get update
sudo apt-get install ./docker-desktop-amd64.deb
```
4. Check Docker Version

```bash
$ docker --version
Docker version 28.3.3, build 980b856
```

5. 


## Jenkins Installation Process

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


## Kubernetes - kubectl Installation Process

Installing kubectl on Ubuntu 24.04.3 LTS

1. Download kubectl binary
```bash
$ curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

```
2. Install kubectl

```bash
$ sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
```

3. Test to ensure the version you installed is up-to-date:

```bash
$ kubectl version --client
```

Or use this for detailed view of version:

```bash
$ kubectl version --client --output=yaml
```

## Kubernetes - minikube Installation Process

Installing minikube on Ubuntu 24.04.3 LTS

1. Download binary binary
```bash
$ curl -LO https://github.com/kubernetes/minikube/releases/latest/download/minikube-linux-amd64

```
2. Install minikube

```bash
$ sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

3. Check version

```bash
$ minikube version
```

4. start m,inikuiibe with docker as driver( Install Docker Before use this command) :

```bash
$ minikube start --driver=docker
```
if get following output then next command using force

```bash
minikube start --driver=docker
😄  minikube v1.36.0 on Ubuntu 24.04
✨  Using the docker driver based on user configuration
🛑  The "docker" driver should not be used with root privileges. If you wish to continue as root, use --force.
💡  If you are running minikube within a VM, consider using --driver=none:
📘    https://minikube.sigs.k8s.io/docs/reference/drivers/none/

❌  Exiting due to DRV_AS_ROOT: The "docker" driver should not be used with root privileges.
```
this command force to use docker as driver

```bash
$ minikube start --driver=docker --force
```


