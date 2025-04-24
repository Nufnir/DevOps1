# Installation of Kubernetes on a single VM

0. Make sure to use a static IP address.
1. Installing updates and utils:
```bash
sudo apt update && sudo apt upgrade -y
```
```bash
sudo apt install curl wget net-tools iproute2 vim git -y
```
2. Installing DockerCE
```bash
sudo apt-get remove docker docker-engine docker.io containerd runc
```
```bash
sudo apt-get update
```
```bash
sudo apt-get install ca-certificates curl gnupg lsb-release
```
```bash
sudo mkdir -m 0755 -p /etc/apt/keyrings
```
```bash
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
```bash
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
```bash
sudo apt-get update
```
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io
```
3. Disabling swap
```bash
sudo swapoff -a
```
4. 
