---
title: Release | Kubed
description: kubed Release
menu:
  docs_v0.11.0:
    identifier: release
    name: Release
    parent: developer-guide
    weight: 15
product_name: kubed
menu_name: docs_v0.11.0
section_menu_id: setup
info:
  version: v0.11.0
---

# Release Process

The following steps must be done from a Linux x64 bit machine.

- Do a global replacement of tags so that docs point to the next release.
- Push changes to the `release-x` branch and apply new tag.
- Push all the changes to remote repo.
- Build and push kubed docker image:
```console
$ cd ~/go/src/github.com/appscode/kubed
$ env APPSCODE_ENV=prod ./hack/make.py build
$ ./hack/docker/setup.sh; env APPSCODE_ENV=prod ./hack/docker/setup.sh release
```

- Now, update the release notes in Github. See previous release notes to get an idea what to include there.
