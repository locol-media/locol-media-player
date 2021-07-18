Overview
===

These are the notes to get the Locol Media Player running on a computer with *Ubuntu Desktop*


Here is documentation for K3s: https://rancher.com/docs/k3s/latest/en/

Install k3s
===
```
curl -sfL https://get.k3s.io | sh -
```

To set up monitoring in Lens (optional but recommended)
===
* Down Lens onto a convenient machine for monitoring the player. https://k8slens.dev/
* Make a copy of /etc/rancher/k3s/k3s.yaml from the k8s server.
* Change url inside so that it is accessable from your machine with Lens
* paste into Lens 'Add cluster" screen

To enable local kubectl (optional? Or use sudo kubectl?)
===
kubectl get pods -- get error msg Unable to read /etc/rancher/k3s/k3s.yaml, to bypass
```
sudo chmod 644 /etc/rancher/k3s/k3s.yaml
```

To install the locol media player
===
On the k3s server, git clone the repo into the server and deploy the agent, deploy into the k3s cluster
```
git clone https://github.com/locol-media/locol-media-player.git
kubectl apply -f locol-media-player/yaml/locol-player-core-installation.yaml
```

To start the locol location admin screen
===
```
(One time only: make the script executable)
sudo chmod a+x locol-media-player/bootstrap.sh
```
Run the bootstrap script
```
./locol-media-player/bootstrap.sh

```