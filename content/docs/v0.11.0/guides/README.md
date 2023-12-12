---
title: Overview
description: Overview of guides
menu:
  docs_v0.11.0:
    identifier: guides-overview
    name: Overview
    parent: guides
    weight: -1
product_name: kubed
menu_name: docs_v0.11.0
section_menu_id: guides
url: /docs/v0.11.0/guides/
aliases:
- /docs/v0.11.0/guides/README/
info:
  version: v0.11.0
---

# Guides

This section contains guides on how to use Kubed. Please visit the links below to learn more:

- Disaster Recovery
  - [Cluster Snapshots](/docs/v0.11.0/guides/disaster-recovery/cluster-snapshot): This tutorial will show you how to use Kubed to take periodic snapshots of a Kubernetes cluster objects.
  - [Kubernetes Recycle Bin](/docs/v0.11.0/guides/disaster-recovery/recycle-bin): Kubed provides a recycle bin for deleted and/or updated Kubernetes objects. This tutorial will show you how to use Kubed to setup a recycle bin for Kubernetes cluster objects.
  - [Backup & Restore Persistent Volumes](/docs/v0.11.0/guides/disaster-recovery/stash). Use [Stash](https://appscode.com/products/stash) to backup & restore Persistent Volumes.
- Configuration Syncer
  - [Synchronize Configuration across Namespaces](/docs/v0.11.0/guides/config-syncer/intra-cluster): This tutorial will show you how Kubed can sync ConfigMaps/Secrets across Kubernetes namespaces.
  - [Synchronize Configuration across Clusters](/docs/v0.11.0/guides/config-syncer/inter-cluster): This tutorial will show you how Kubed can sync ConfigMaps/Secrets across Kubernetes cluster.
- Cluster Events
  - [Forward Cluster Events](/docs/v0.11.0/guides/cluster-events/event-forwarder): This tutorial will show you how to use Kubed to send notifications via Email, SMS or Chat for various cluster events.
  - [Supported Notifiers](/docs/v0.11.0/guides/cluster-events/notifiers): This article documents how to configure Kubed to send notifications via Email, SMS or Chat
- [Using Janitors](/docs/v0.11.0/guides/janitors): Kubernetes supports storing cluster logs in Elasticsearch and cluster metrics in InfluxDB. This tutorial will show you how to use kubed janitors to delete old data from Elasticsearch and InfluxDB.
- [Kubed API Server](/docs/v0.11.0/guides/apiserver): This article documents various aspects of Kubed api server.
- [Monitoring Kubed](/docs/v0.11.0/guides/monitoring): This article described the various metrics exposed by Kubed operator.
