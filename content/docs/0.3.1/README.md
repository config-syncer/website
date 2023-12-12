[![Go Report Card](https://goreportcard.com/badge/github.com/appscode/kubed)](https://goreportcard.com/report/github.com/appscode/kubed)

# Kubed
Kubed (pronounced Cube-Dee) by AppsCode is a Kubernetes Cluster Operator Daemon. Kubed can do the following things for you:

 - Kubed can take periodic [snapshot](/docs/0.3.1/tutorials/cluster-snapshot) of a Kubernetes cluster objects.
 - Kubed provides a [recycle bin](/docs/0.3.1/tutorials/recycle-bin) for deleted and/or updated Kubernetes objects.
 - Kubed can keep [ConfigMaps and Secrets synchronized across Namespaces](/docs/0.3.1/tutorials/config-syncer).
 - Kubed can [forward cluster events](/docs/0.3.1/tutorials/event-forwarder) to various destinations.
 - Kubed can setup [janitors](/docs/0.3.1/tutorials/janitors) for Elasticsearch and InfluxDB.
 - Kubed can [send notifications](/docs/0.3.1/tutorials/notifiers) via Email, SMS or Chat.
 - Kubed has a built-in [search engine](/docs/0.3.1/tutorials/apiserver) for your cluster objects using [bleve](https://github.com/blevesearch/bleve).

## Supported Versions
Please pick a version of Kubed that matches your Kubernetes installation.

| Kubed Version                                                 | Docs                                                            | Kubernetes Version |
|---------------------------------------------------------------|-----------------------------------------------------------------|--------------------|
| [0.3.1](https://github.com/appscode/kubed/releases/tag/0.3.1) | [User Guide](https://github.com/appscode/kubed/tree/0.3.1/docs) | 1.7.x+             |
| [0.2.0](https://github.com/appscode/kubed/releases/tag/0.2.0) | [User Guide](https://github.com/appscode/kubed/tree/0.2.0/docs) | 1.5.x - 1.7.x      |

## Installation
To install Kubed, please follow the guide [here](/docs/0.3.1/install).

## Using Kubed
Want to learn how to use Kubed? Please start [here](/docs/0.3.1/tutorials/README).

## Contribution guidelines
Want to help improve Kubed? Please start [here](/CONTRIBUTING.md).

## Project Status
Wondering what features are coming next? Please visit [here](/ROADMAP.md).

---

**The kubed operator collects anonymous usage statistics to help us learn how the software is being used and how we can improve it. To disable stats collection, run the operator with the flag** `--analytics=false`.

---

## Support
If you have any questions, you can reach out to us.
* [Slack](https://slack.appscode.com)
* [Twitter](https://twitter.com/AppsCodeHQ)
* [Website](https://appscode.com)
