---
title: Config-Syncer
menu:
  docs_v0.14.4:
    identifier: config-syncer
    name: Config-Syncer
    parent: reference
    weight: 0
product_name: kubed
menu_name: docs_v0.14.4
section_menu_id: reference
aliases:
- /docs/v0.14.4/reference/
info:
  version: v0.14.4
---

## config-syncer

Config Syncer by AppsCode - A Kubernetes Configuration Syncer

### Synopsis

Config Syncer is a Kubernetes controller to sync configmaps and secrets. For more information, visit here: https://github.com/kubeops/config-syncer/tree/master/docs

### Options

```
  -h, --help                             help for config-syncer
      --use-kubeapiserver-fqdn-for-aks   if true, uses kube-apiserver FQDN for AKS cluster to workaround https://github.com/Azure/AKS/issues/522 (default true)
```

### SEE ALSO

* [config-syncer run](/docs/v0.14.4/reference/config-syncer_run)	 - Launch Kubernetes Cluster Daemon
* [config-syncer version](/docs/v0.14.4/reference/config-syncer_version)	 - Prints binary version number.

