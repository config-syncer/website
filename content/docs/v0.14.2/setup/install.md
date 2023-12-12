---
title: Config Syncer Install
description: Config Syncer Install
menu:
  docs_v0.14.2:
    identifier: kubed-install
    name: Install
    parent: setup
    weight: 10
product_name: kubed
menu_name: docs_v0.14.2
section_menu_id: setup
info:
  version: v0.14.2
---

> New to Config Syncer? Please start [here](/docs/v0.14.2/concepts/README).

# Installation Guide

Config Syncer operator can be installed via a script or as a Helm chart.

<ul class="nav nav-tabs" id="installerTab" role="tablist">
  <li class="nav-item">
    <a class="nav-link active" id="helm3-tab" data-toggle="tab" href="#helm3" role="tab" aria-controls="helm3" aria-selected="true">Helm 3 (Recommended)</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="script-tab" data-toggle="tab" href="#script" role="tab" aria-controls="script" aria-selected="false">YAML</a>
  </li>
</ul>
<div class="tab-content" id="installerTabContent">
  <div class="tab-pane fade show active" id="helm3" role="tabpanel" aria-labelledby="helm3-tab">

## Using Helm 3

Config Syncer can be installed via [Helm](https://helm.sh/) using the [chart](https://github.com/kubeops/config-syncer/tree/{{< param "info.version" >}}/charts/config-syncer) from [AppsCode Charts Repository](https://github.com/appscode/charts). To install the chart with the release name `kubed`:

```bash
$ helm install config-syncer \
  oci://ghcr.io/appscode-charts/config-syncer \
  --version {{< param "info.version" >}} \
  --namespace kubeops --create-namespace \
  --set-file license=/path/to/the/license.txt \
  --wait --burst-limit=10000 --debug
```

To see the detailed configuration options, visit [here](https://github.com/kubeops/config-syncer/tree/{{< param "info.version" >}}/charts/config-syncer).

</div>
<div class="tab-pane fade" id="script" role="tabpanel" aria-labelledby="script-tab">

## Using YAML

If you prefer to not use Helm, you can generate YAMLs from Config Syncer chart and deploy using `kubectl`. Here we are going to show the prodecure using Helm 3.

```bash
$ helm template config-syncer \
  oci://ghcr.io/appscode-charts/config-syncer \
  --version {{< param "info.version" >}} \
  --namespace kubeops --create-namespace \
  --set-file license=/path/to/the/license.txt \
  --no-hooks | kubectl apply -f -
```

To see the detailed configuration options, visit [here](https://github.com/kubeops/config-syncer/tree/{{< param "info.version" >}}/charts/config-syncer).

</div>
</div>

### Installing in GKE Cluster

If you are installing Config Syncer on a GKE cluster, you will need cluster admin permissions to install Config Syncer operator. Run the following command to grant admin permision to the cluster.

```bash
$ kubectl create clusterrolebinding "cluster-admin-$(whoami)" \
  --clusterrole=cluster-admin \
  --user="$(gcloud config get-value core/account)"
```

In addition, if your GKE cluster is a [private cluster](https://cloud.google.com/kubernetes-engine/docs/how-to/private-clusters), you will need to either add an additional firewall rule that allows master nodes access port `8443/tcp` on worker nodes, or change the existing rule that allows access to ports `443/tcp` and `10250/tcp` to also allow access to port `8443/tcp`. The procedure to add or modify firewall rules is described in the official GKE documentation for private clusters mentioned before.

## Verify installation

Config Syncer includes a check command to verify a cluster config. Download the pre-built binary from [config-syncer Github releases](https://github.com/kubeops/config-syncer/releases) and put the binary to some directory in your `PATH`.

```bash
$ kubed check --clusterconfig=./hack/deploy/config.yaml
Cluster config was parsed successfully.
```