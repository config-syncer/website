---
title: Kubed Run
menu:
  docs_0.5.0:
    identifier: kubed-run
    name: Kubed Run
    parent: reference
product_name: kubed
menu_name: docs_0.5.0
section_menu_id: reference
info:
  version: 0.5.0
---

## kubed run

Run daemon

### Synopsis

Run daemon

```
kubed run [flags]
```

### Options

```
      --api.address string               The address of the Kubed API Server (overrides any value in clusterconfig) (default ":8080")
      --burst int                        The maximum burst for throttle (default 1000000)
      --clusterconfig string             Path to cluster config file (default "/srv/kubed/config.yaml")
  -h, --help                             help for run
      --kubeconfig string                Path to kubeconfig file with authorization information (the master location is set by the master flag).
      --master string                    The address of the Kubernetes API server (overrides any value in kubeconfig)
      --prometheus-crd-apigroup string   prometheus CRD  API group name (default "monitoring.coreos.com")
      --prometheus-crd-kinds CrdKinds     - EXPERIMENTAL (could be removed in future releases) - customize CRD kind names
      --qps float32                      The maximum QPS to the master from this client (default 1e+06)
      --resync-period duration           If non-zero, will re-list this often. Otherwise, re-list will be delayed aslong as possible (until the upstream source closes the watch or times out. (default 5m0s)
      --scratch-dir emptyDir             Directory used to store temporary files. Use an emptyDir in Kubernetes. (default "/tmp")
      --web.address string               Address to listen on for web interface and telemetry. (default ":56790")
```

### Options inherited from parent commands

```
      --alsologtostderr                  log to standard error as well as files
      --analytics                        Send analytical events to Google Analytics (default true)
      --log_backtrace_at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log_dir string                   If non-empty, write log files in this directory
      --logtostderr                      log to standard error instead of files
      --stderrthreshold severity         logs at or above this threshold go to stderr (default 2)
  -v, --v Level                          log level for V logs
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [kubed](/docs/0.5.0/reference/kubed)	 - Kubed by AppsCode - A Kubernetes Cluster Operator Daemon

