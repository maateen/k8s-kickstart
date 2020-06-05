# k8s-kickstart
An Ansible Playbook which gifts you all components you require on K8s cluster.

## Requirements

- K8s Cluster

Intall dependencies to run the playbook:

```shell
$ pip3 install -r requirements.txt
$ ansible-galaxy collection install -r requirements.yaml
```

## Usage

```shell
$ ansible-playbook playbook.yaml
```

## Roadmap

- [x] Setup Pod Network Add-on (CNI)
    - [x] Calico
    - [x] Cilium
    - [x] Flannel
    - [x] Weave
- [x] Setup Namespace
- [x] Setup Ingress Controller
    - [ ] Ambassador
    - [x] NginX
    - [x] Traefik
    - [ ] Voyager
- [ ] Setup Logging Stack
    - [ ] Elasticsearch
    - [ ] Fluentbit
    - [ ] Fluentd
    - [ ] Kibana
    - [ ] Logstash
- [ ] Setup Monitoring Stack
    - [ ] Alertmanager
    - [ ] Prometheus
    - [ ] Grafana