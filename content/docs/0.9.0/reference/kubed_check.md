---
title: Kubed Check
menu:
  docs_0.9.0:
    identifier: kubed-check
    name: Kubed Check
    parent: reference
product_name: kubed
menu_name: docs_0.9.0
section_menu_id: reference
info:
  version: 0.9.0
---

## kubed check

Check cluster config

### Synopsis

Check cluster config

```
kubed check [flags]
```

### Options

```
      --clusterconfig string   Path to cluster config file
  -h, --help                   help for check
```

### Options inherited from parent commands

```
      --alsologtostderr                  log to standard error as well as files
      --enable-analytics                 send usage events to Google Analytics (default true)
      --log-flush-frequency duration     Maximum number of seconds between log flushes (default 5s)
      --log.format logFormatFlag         Set the log target and format. Example: "logger:syslog?appname=bob&local=7" or "logger:stdout?json=true" (default "logger:stderr")
      --log.level levelFlag              Only log messages with the given severity or above. Valid levels: [debug, info, warn, error, fatal] (default "info")
      --log_backtrace_at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log_dir string                   If non-empty, write log files in this directory
      --logtostderr                      log to standard error instead of files (default true)
      --stderrthreshold severity         logs at or above this threshold go to stderr
      --use-kubeapiserver-fqdn-for-aks   if true, uses kube-apiserver FQDN for AKS cluster to workaround https://github.com/Azure/AKS/issues/522 (default true)
  -v, --v Level                          log level for V logs
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [kubed](/docs/0.9.0/reference/kubed)	 - Kubed by AppsCode - A Kubernetes Cluster Operator Daemon

