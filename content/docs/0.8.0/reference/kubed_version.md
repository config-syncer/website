---
title: Kubed Version
menu:
  docs_0.8.0:
    identifier: kubed-version
    name: Kubed Version
    parent: reference
product_name: kubed
menu_name: docs_0.8.0
section_menu_id: reference
info:
  version: 0.8.0
---

## kubed version

Prints binary version number.

### Synopsis

Prints binary version number.

```
kubed version [flags]
```

### Options

```
  -h, --help    help for version
      --short   Print just the version number.
```

### Options inherited from parent commands

```
      --alsologtostderr                  log to standard error as well as files
      --enable-analytics                 send usage events to Google Analytics (default true)
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

* [kubed](/docs/0.8.0/reference/kubed)	 - Kubed by AppsCode - A Kubernetes Cluster Operator Daemon

