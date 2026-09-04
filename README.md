# K8S-ON-AWS
# K8S ON AWS

- Create an EC2 instance machine — m7i flex large, Ubuntu — and create a key pair. Paste in Users -> user.
- Open PWS terminal in user.

ssh -i "K8S.pem" ubuntu@16.16.214.117
```

sudo apt update && sudo apt upgrade -y   # update all packages to latest version
sudo apt install -y docker.io            # install docker engine, required by minikube to start containers

curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo systemctl enable docker
sudo systemctl start docker
sudo usermod -aG docker ubuntu
```

exit and login

## FOR KUBECTL
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
kubectl version --client
```

## FOR MINIKUBE
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
rm minikube-linux-amd64
minikube version
```

## FOR CONNTRACK
sudo apt update
sudo apt install -y conntrack
```

minikube start --driver=docker
```

## TO CLEAN SPACE

docker system prune -a --volumes -f
sudo apt clean
sudo rm -rf /var/lib/apt/lists/*
```
kubectl get nodes
```
