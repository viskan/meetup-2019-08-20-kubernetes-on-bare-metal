# Viskan Meetup 2019-08-20: Kubernetes on bare metal

Slides can be found [here](https://docs.google.com/presentation/d/1vY6zNNfqQXXBz10egJDRS-vJoRXK0mhxFkdMvlFNW0o).


## Preparation

```shell
$ mkdir --parents ~/projects
$ cd ~/projects
$ git clone git@github.com:viskan/meetup-2019-08-20-kubernetes-on-bare-metal.git
$ git clone git@github.com:amimof/kubernetes-the-right-way.git
$ cd ~/projects/kubernetes-the-right-way
$ git checkout v1.0.4
```


## Installing

```shell
$ cd ~/projects/meetup-2019-08-20-kubernetes-on-bare-metal
$ ansible-playbook --inventory ansible-inventory --ask-pass --ask-become-pass \
     ~/projects/kubernetes-the-right-way/install.yml
```


## Installing manifests

```
$ cd manifests
$ KUBECONFIG=~/.ktrw/k8s-lab/kubeconfig kubectl apply -f flannel
$ KUBECONFIG=~/.ktrw/k8s-lab/kubeconfig kubectl apply -f nginx-ingress-controller
$ KUBECONFIG=~/.ktrw/k8s-lab/kubeconfig kubectl apply -f who-am-i
```
