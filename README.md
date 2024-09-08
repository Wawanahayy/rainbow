# rainbow protocol

#install

```bash
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

# create/clone repo
```bash
mkdir -p /root/project/run_btc_testnet4/data
git clone https://github.com/rainbowprotocol-xyz/btc_testnet4
cd btc_testnet4
```

# BITCOIN core or docker-compose install
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
```bash
sudo chmod +x /usr/local/bin/docker-compose
```

# Start Bitcoin Core by running
```bash
docker-compose up -d
```
```bash
docker exec -it bitcoind /bin/bash
```
```bash
bitcoin-cli -testnet4 -rpcuser=JUEPE -rpcpassword=JEPE -rpcport=5000 createwallet JACKPOT
```
