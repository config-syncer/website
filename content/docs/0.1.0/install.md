> New to Kubed? Please start [here](/docs/0.1.0/tutorials/README).

# Installation Guide

## Create Cluster Config
Before you can install Kubed, you need a cluster config for Kubed. Cluster config is defined in YAML format. You find an example config in [./hack/deploy/config.yaml](/hack/deploy/config.yaml).

```yaml
$ cat ./hack/deploy/config.yaml

apiServer:
  address: :8080
  enableReverseIndex: true
  enableSearchIndex: true
enableConfigSyncer: true
eventForwarder:
  ingressAdded:
    handle: true
  nodeAdded:
    handle: true
  receivers:
  - notifier: mailgun
    to:
    - ops@example.com
  storageAdded:
    handle: true
  warningEvents:
    handle: true
    namespaces:
    - kube-system
janitors:
- elasticsearch:
    endpoint: http://elasticsearch-logging.kube-system:9200
    logIndexPrefix: logstash-
  kind: Elasticsearch
  ttl: 2160h0m0s
- influxdb:
    endpoint: https://monitoring-influxdb.kube-system:8086
  kind: InfluxDB
  ttl: 2160h0m0s
notifierSecretName: notifier-config
recycleBin:
  handleUpdates: false
  path: /tmp/kubed/trash
  receivers:
  - notifier: mailgun
    to:
    - ops@example.com
  ttl: 168h0m0s
snapshotter:
  gcs:
    bucket: restic
    prefix: minikube
  storageSecretName: snap-secret
  sanitize: true
  schedule: '@every 6h'
```

To understand the various configuration options, check Kubed [tutorials](/docs/0.1.0/tutorials/README). Once you are satisfied with the configuration, create a Secret with the Kubed cluster config under `config.yaml` key.

You may have to create another [Secret for notifiers](/docs/0.1.0/tutorials/notifiers), usually called `notifier-config`. If you are [storing cluster snapshots](/docs/0.1.0/tutorials/cluster-snapshot) in cloud storage, you have to create another Secret to provide cloud credentials.

### Generate Config using script
If you are familiar with GO, you can use the [./hack/config/main.go](/hack/config/main.go) script to generate a cluster config. Open this file in your favorite editor, update the config returned from `#CreateClusterConfig()` method. Then run the script to generate updated config in [./hack/deploy/config.yaml](/hack/deploy/config.yaml).

```console
go run ./hack/config/main.go
```

### Verifying Cluster Config
Kubed includes a check command to verify a cluster config. Download the pre-built binary from [appscode/kubed Github releases](https://github.com/appscode/kubed/releases) and put the binary to some directory in your `PATH`.

```console
$ kubed check --clusterconfig=./hack/deploy/config.yaml
Cluster config was parsed successfully.
```

## Using YAML
Kubed can be installed using YAML files includes in the [/hack/deploy](/hack/deploy) folder.

```console
# Install without RBAC roles
$ curl https://raw.githubusercontent.com/appscode/kubed/0.1.0/hack/deploy/without-rbac.yaml \
  | kubectl apply -f -


# Install with RBAC roles
$ curl https://raw.githubusercontent.com/appscode/kubed/0.1.0/hack/deploy/with-rbac.yaml \
  | kubectl apply -f -
```

## Using Helm
Kubed can be installed via [Helm](https://helm.sh/) using the [chart](/chart/kubed) included in this repository. To install the chart with the release name `my-release`:
```bash
$ helm install chart/kubed --name my-release
```
To see the detailed configuration options, visit [here](/chart/kubed/README.md).


## Verify installation
To check if Kubed operator pods have started, run the following command:
```console
$ kubectl get pods --all-namespaces -l app=kubed --watch
```

Once the operator pods are running, you can cancel the above command by typing `Ctrl+C`.


## Update Cluster Config
If you would like to update cluster config, update the `kubed-config` Secret and restart Kubed operator pod(s).
