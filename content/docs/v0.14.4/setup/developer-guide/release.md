---
title: Release | Config Syncer
description: kubed Release
menu:
  docs_v0.14.4:
    identifier: release
    name: Release
    parent: developer-guide
    weight: 15
product_name: kubed
menu_name: docs_v0.14.4
section_menu_id: setup
info:
  version: v0.14.4
---

# Release Process

The following steps must be done from a Linux x64 bit machine.

- Do a global replacement of tags so that docs point to the next release.
- Push changes to the `release-x` branch and apply new tag.
- Push all the changes to remote repo.
- Build and push kubed docker image:
```bash
$ cd ~/go/src/kubeops.dev/config-syncer
$ env APPSCODE_ENV=prod ./hack/make.py build
$ ./hack/docker/setup.sh; env APPSCODE_ENV=prod ./hack/docker/setup.sh release
```

- Now, update the release notes in Github. See previous release notes to get an idea what to include there.
