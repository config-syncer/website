---
title: Kubed
menu:
  docs_0.7.0:
    identifier: kubed
    name: Kubed
    parent: reference
    weight: 0
product_name: kubed
menu_name: docs_0.7.0
section_menu_id: reference
aliases:
- /docs/0.7.0/reference/
info:
  version: 0.7.0
---

## kubed

Kubed by AppsCode - A Kubernetes Cluster Operator Daemon

### Synopsis

Kubed is a Kubernetes daemon to perform cluster management tasks. For more information, visit here: https://github.com/appscode/kubed/tree/master/docs

### Options

```
      --alsologtostderr                  log to standard error as well as files
      --enable-analytics                 send usage events to Google Analytics (default true)
  -h, --help                             help for kubed
      --log.format logFormatFlag         Set the log target and format. Example: "logger:syslog?appname=bob&local=7" or "logger:stdout?json=true" (default "logger:stderr")
      --log.level levelFlag              Only log messages with the given severity or above. Valid levels: [debug, info, warn, error, fatal] (default "info")
      --log_backtrace_at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log_dir string                   If non-empty, write log files in this directory
      --logtostderr                      log to standard error instead of files
      --stderrthreshold severity         logs at or above this threshold go to stderr (default 2)
  -v, --v Level                          log level for V logs
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [kubed backup](/docs/0.7.0/reference/kubed_backup)	 - Takes a backup of Kubernetes api objects
* [kubed check](/docs/0.7.0/reference/kubed_check)	 - Check cluster config
* [kubed run](/docs/0.7.0/reference/kubed_run)	 - Launch Kubernetes Cluster Daemon
* [kubed version](/docs/0.7.0/reference/kubed_version)	 - Prints binary version number.

