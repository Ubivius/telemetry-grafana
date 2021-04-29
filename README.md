# telemetry-grafana

A dashboard manager to display all the relevant informations to enable your team to deploy and diagnose the cluster's content

# Grafana Helm Chart

- grafana · grafana/grafana (https://artifacthub.io/packages/helm/grafana/grafana)

## Get Repo Info

```console
$ helm repo add grafana https://grafana.github.io/helm-charts
$ helm repo update
```

## Installing the Chart

To install the chart with the release name `grafana`:

```console
$ helm install grafana --version <version> grafana/grafana -f chart/values.yaml
```

## Grafana password

Get your 'admin' user password by running:

```console
$ kubectl get secret --namespace default grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo
```

## Uninstalling the Chart

To uninstall/delete the grafana deployment:

```console
$ helm delete grafana
```

The command removes all the Kubernetes components associated with the chart and deletes the release.
