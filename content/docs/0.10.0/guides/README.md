---
title: Overview
description: Overview of guides
menu:
  docs_0.10.0:
    identifier: guides-overview
    name: Overview
    parent: guides
    weight: -1
product_name: kubed
menu_name: docs_0.10.0
section_menu_id: guides
url: /docs/0.10.0/guides/
aliases:
- /docs/0.10.0/guides/README/
info:
  version: 0.10.0
---

# Guides

This section contains guides on how to use Kubed. Please visit the links below to learn more:

- Disaster Recovery
  - [Cluster Snapshots](/docs/0.10.0/guides/disaster-recovery/cluster-snapshot): This tutorial will show you how to use Kubed to take periodic snapshots of a Kubernetes cluster objects.
  - [Kubernetes Recycle Bin](/docs/0.10.0/guides/disaster-recovery/recycle-bin): Kubed provides a recycle bin for deleted and/or updated Kubernetes objects. This tutorial will show you how to use Kubed to setup a recycle bin for Kubernetes cluster objects.
  - [Backup & Restore Persistent Volumes](/docs/0.10.0/guides/disaster-recovery/stash). Use [Stash](https://appscode.com/products/stash) to backup & restore Persistent Volumes.
- Configuration Syncer
  - [Synchronize Configuration across Namespaces](/docs/0.10.0/guides/config-syncer/intra-cluster): This tutorial will show you how Kubed can sync ConfigMaps/Secrets across Kubernetes namespaces.
  - [Synchronize Configuration across Clusters](/docs/0.10.0/guides/config-syncer/inter-cluster): This tutorial will show you how Kubed can sync ConfigMaps/Secrets across Kubernetes cluster.
- Cluster Events
  - [Forward Cluster Events](/docs/0.10.0/guides/cluster-events/event-forwarder): This tutorial will show you how to use Kubed to send notifications via Email, SMS or Chat for various cluster events.
  - [Supported Notifiers](/docs/0.10.0/guides/cluster-events/notifiers): This article documents how to configure Kubed to send notifications via Email, SMS or Chat
- [Using Janitors](/docs/0.10.0/guides/janitors): Kubernetes supports storing cluster logs in Elasticsearch and cluster metrics in InfluxDB. This tutorial will show you how to use kubed janitors to delete old data from Elasticsearch and InfluxDB.
- [Kubed API Server](/docs/0.10.0/guides/apiserver): This article documents various aspects of Kubed api server.
- [Monitoring Kubed](/docs/0.10.0/guides/monitoring): This article described the various metrics exposed by Kubed operator.
