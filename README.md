# Chart

[![Chart Release](https://github.com/marsfield-labs/charts/actions/workflows/build-chart.yaml/badge.svg)](https://github.com/marsfield-labs/charts/actions/workflows/build-chart.yaml)

This is git repo of available charts published for users.

## List of charts

Here is a list of charts available:

  Name  | Description
--------|-----------------
rtl-poc | rtl poc project
multi-k8s | multi-k8s

## Add repo using helm

First, add our charts to the repo list.

```sh
helm repo add marsfield-labs https://marsfield-labs.github.io/charts
```

## References

* [Helm](https://helm.sh)
* [Release chart using github action](https://helm.sh/docs/howto/chart_releaser_action/)
