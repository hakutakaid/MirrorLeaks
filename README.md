```
sudo apt update
```

```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```
apt-cache policy docker-ce
```

```
sudo apt install docker-ce
```

```
sudo systemctl status docker
```

## Deploy
```
apt install python3-pip
```
```
git clone https://github.com/hakutakaid/MirrorLeaks
```
```
cd MirrorLeaks
```
```
pip3 install -r requirements-cli.txt
```

## config edit
```
cp config_sample.py config.py
```
## RUNNING DOCKER

```
sudo docker build . -t mltb
```
```
sudo docker run --network host mltb
```


## STOP DOCKER

```
docker ps
```
```
dokcer stop UID
```
```
docker rm $(docker ps -aq)
```
```
docker rmi $(docker images -q)
```
```
docker rmi -f $(docker images -q)
```
```
docker builder prune --all
```
