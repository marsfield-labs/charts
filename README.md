# Charts by Marsfield Labs

[![Chart Release](https://github.com/marsfield-labs/charts/actions/workflows/build-chart.yaml/badge.svg)](https://github.com/marsfield-labs/charts/actions/workflows/build-chart.yaml)

This repo is a self-hosted [Helm](https://helm.sh) charts repo of [marsfield-labs](https://github.com/marsfield-labs).

## Repo setup

In order to use a github repo as self-hosted helm charts repo, we need to configure it as below:

* make it public
* add branch `gh-pages` and use it as source for project page
* add workflow and use `helm-chart-releaser` to publish charts
* if chart source files are not under `/charts`, then specify `charts_dir` as workflow input

## List of charts

Here is a list of charts that are currently available:

  Name  | Description
--------|-----------------
demo    | A simple echo server
multi-k8s | A toy project that illustrate complex container composition
rtl-poc | A demonstration Rewards-to-Loyalty project

## Add repo using helm

Once `index.yaml` has been deployed as project page, we are able to add it as a helm repo to the kubernetes cluster.

```sh
helm repo add marsfield-labs https://marsfield-labs.github.io/charts
```

Next, we can run `update`, to retrieve the latest charts information, like below:

```sh
helm repo update marsfield-labs
```

To see what charts are available, run:

```sh
helm search repo marsfield-labs
```

## References

* [Helm](https://helm.sh)
* [Release chart using github action](https://helm.sh/docs/howto/chart_releaser_action/)
* [Helm Installer](https://github.com/marketplace/actions/helm-tool-installer)
* [Helm Releaser](https://github.com/marketplace/actions/helm-chart-releaser)
* [Hosting pages on github](https://pages.github.com/)
* [GitHub Pages documentation](https://docs.github.com/en/pages)
