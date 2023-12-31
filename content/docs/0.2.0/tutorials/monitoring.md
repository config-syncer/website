> New to Kubed? Please start [here](/docs/0.2.0/tutorials/README).

# Monitoring Kubed

Kubed has native support for monitoring via Prometheus. Kubed operator exposes Prometheus native monitoring data via `/metrics` endpoint on `:56790` port. You can setup a [CoreOS Prometheus ServiceMonitor](https://github.com/coreos/prometheus-operator) using `kubed-operator` service. To change the port, use `--web.address` flag on Kubed operator.

```console
$ kubectl get pods -n kube-system
NAME                              READY     STATUS    RESTARTS   AGE
kube-addon-manager-minikube       1/1       Running   0          33m
kube-dns-1301475494-hglm0         3/3       Running   0          33m
kubed-operator-3234987584-sbgrf   1/1       Running   0          19s
kubernetes-dashboard-l8vlj        1/1       Running   0          33m


$ kubectl port-forward $(kubectl get pods --all-namespaces -l app=kubed -o jsonpath={.items[0].metadata.name}) -n kube-system 56790
Forwarding from 127.0.0.1:56790 -> 56790
E0727 03:50:34.668103   22871 portforward.go:212] Unable to create listener: Error listen tcp6 [::1]:56790: bind: cannot assign requested address
Handling connection for 56790
```

Now, open the URL [http://127.0.0.1:56790/metrics](http://127.0.0.1:56790/metrics) in your browser.


## Next Steps
 - Learn how to use Kubed to take periodic snapshots of a Kubernetes cluster [here](/docs/0.2.0/tutorials/cluster-snapshot).
 - To setup a recycle bin for deleted and/or updated Kubernetes objects, please visit [here](/docs/0.2.0/tutorials/recycle-bin).
 - Need to keep some configuration synchronized across namespaces? Try [Kubed config syncer](/docs/0.2.0/tutorials/config-syncer).
 - Want to keep an eye on your cluster with automated notifications? Setup Kubed [event forwarder](/docs/0.2.0/tutorials/event-forwarder).
 - Out of disk space because of too much logs in Elasticsearch or metrics in InfluxDB? Configure [janitors](/docs/0.2.0/tutorials/janitors) to delete old data.
 - See the list of supported notifiers [here](/docs/0.2.0/tutorials/notifiers).
 - Wondering what features are coming next? Please visit [here](/ROADMAP.md).
 - Want to hack on Kubed? Check our [contribution guidelines](/CONTRIBUTING.md).
