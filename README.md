# k8s-kickstart
An Ansible Playbook which gifts you all components you require on K8s cluster.

## Requirements

- Kubernetes (>= 1.6)
- Helm3

Intall dependencies to run the playbook:

```shell
$ pip3 install -r requirements.txt
$ ansible-galaxy collection install -r requirements.yaml
```

## Usage

```shell
$ ansible-playbook playbook.yaml
```

## Ansible Variables

| Variable| Default | Supported Variables |
| ------- | ------- | ------------------- |
| setup_cni | `false` | `true`, `false` |
| cni_provider | `flannel` | `calico`, `cilium`, `flannel`, `weave` |
| setup_namespace | `true` | `true`, `false` |
| namespaces | `production`, `staging`, `development` | any valid yaml list |
| setup_ingress | `true` | `true`, `false` |
| ingress_provider | `nginx` | `ambassador`, `nginx`, `traefik`, `voyager` |
| ingress_name | `ingress-nginx` | any valid string |
| ingress_namespace | `kube-system` | any valid namespace |

## Roadmap

- [x] Setup Pod Network Add-on (CNI)
    - [x] Calico
    - [x] Cilium
    - [x] Flannel
    - [x] Weave
- [x] Setup Namespace
- [x] Setup Ingress Controller
    - [x] Ambassador
    - [x] NginX
    - [x] Traefik
    - [x] Voyager
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
