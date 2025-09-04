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
