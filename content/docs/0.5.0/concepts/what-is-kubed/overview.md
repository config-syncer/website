---
title: Kubed Overview
description: Kubed Overview
menu:
  docs_0.5.0:
    identifier: overview-concepts
    name: Overview
    parent: what-is-kubed
    weight: 10
product_name: kubed
menu_name: docs_0.5.0
section_menu_id: concepts
info:
  version: 0.5.0
---

# Kubed

Kubed (pronounced Cube-Dee) by AppsCode is a Kubernetes Cluster Operator Daemon. Kubed can do the following things for you:

 - Kubed can protect your Kubernetes cluster from [various disasters scenarios](/docs/0.5.0/guides/disaster-recovery/).
 - Kubed can keep [ConfigMaps and Secrets synchronized across Namespaces](/docs/0.5.0/guides/config-syncer/).
 - Kubed can [forward cluster events](/docs/0.5.0/guides/cluster-events/) to various destinations.
 - Kubed can setup [janitors](/docs/0.5.0/guides/janitors) for Elasticsearch and InfluxDB.
 - Kubed can [send notifications](/docs/0.5.0/guides/cluster-events/notifiers) via Email, SMS or Chat.
 - Kubed has a built-in [search engine](/docs/0.5.0/guides/apiserver) for your cluster objects using [bleve](https://github.com/blevesearch/bleve).
