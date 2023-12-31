---
title: Kubed Uninstall
description: Kubed Uninstall
menu:
  docs_0.5.0:
    identifier: kubed-uninstall
    name: Uninstall
    parent: setup
    weight: 20
product_name: kubed
menu_name: docs_0.5.0
section_menu_id: setup
info:
  version: 0.5.0
---

> New to Kubed? Please start [here](/docs/0.5.0/concepts/README).

# Uninstall Kubed
Please follow the steps below to uninstall Kubed:

- Delete the various objects created for Kubed operator.

```console
$ curl -fsSL https://raw.githubusercontent.com/appscode/kubed/0.5.0/hack/deploy/uninstall.sh | bash

+ kubectl delete deployment -l app=kubed -n kube-system
deployment "kubed-operator" deleted
+ kubectl delete service -l app=kubed -n kube-system
service "kubed-operator" deleted
+ kubectl delete secret -l app=kubed -n kube-system
secret "azure-secret" deleted
secret "kubed-config" deleted
+ kubectl delete serviceaccount -l app=kubed -n kube-system
No resources found
+ kubectl delete clusterrolebindings -l app=kubed -n kube-system
No resources found
+ kubectl delete clusterrole -l app=kubed -n kube-system
No resources found
```

- Now, wait several seconds for Kubed to stop running. To confirm that Kubed operator pod(s) have stopped running, run:

```console
$ kubectl get pods --all-namespaces -l app=kubed
```
