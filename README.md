# Viskan Meetup 2019-08-20: Kubernetes on bare metal

Slides can be found [here](https://docs.google.com/presentation/d/1vY6zNNfqQXXBz10egJDRS-vJoRXK0mhxFkdMvlFNW0o).


## Preparation

```shell
$ mkdir --parents ~/projects
$ cd ~/projects
$ git clone git@github.com:viskan/meetup-k8s-bare-metal.git
$ git clone git@github.com:amimof/kubernetes-the-right-way.git
$ cd ~/projects/kubernetes-the-right-way
$ git checkout v1.0.4
```


## Installing

```shell
$ ansible-playbook --inventory ansible-inventory --ask-pass --ask-become-pass ~/projects/kubernetes-the-right-way/install.yml
```
