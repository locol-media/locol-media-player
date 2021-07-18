## Install k3s

curl -sfL https://get.k3s.io | sh -

## documentation

https://rancher.com/docs/k3s/latest/en/

Install k3s
===
```
curl -sfL https://get.k3s.io | sh -
```

To set up monitoring in Lens (optional)
===
* Make a copy of /etc/rancher/k3s/k3s.yaml
* Change url inside so that it is accessable from your machine with Lens
* paste into Lens 'Add cluster" screen

To enable local kubectl (optional)
===
kubectl get pods -- get error msg Unable to read /etc/rancher/k3s/k3s.yaml, to bypass
```
sudo chmod 644 /etc/rancher/k3s/k3s.yaml
```

To install the locol media player
===
Git clone the repo into the server and deploy the agent.
```
git clone https://github.com/locol-media/locol-media-player.git
```