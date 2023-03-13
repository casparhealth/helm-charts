# Caspar fork

This fork was created in order to fetch lates changes in the `values.ymal` file for Datadog Helm Chart.

To get latest updates from the upstream and merge them into our fork perform next steps on your local machine:

1. Configure upstream remote:

```shell
git remote add upstream https://github.com/DataDog/helm-charts.git
```

2. Fetch upstream

```shell
git fetch upstream
```

3. Checkout to the fork `main` branch

```shell
git checkout main
```

4. Merge upstrem changes into our `main`

```shell
git merge upstream/main
```

5. Resolve conflicts and push

```shell
git push origin main
```

6. Now you can use our updated `charts/datadog/values.yaml` template in the [infrastructure-modules](https://github.com/casparhealth/infrastructure-modules/tree/master/services/k8s-datadog/templates) module.


# Datadog Helm Charts

[![Artifact HUB](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/datadog)](https://artifacthub.io/packages/search?repo=datadog) 

Official Helm charts for Datadog products. Currently supported:
- [Datadog Agents](charts/datadog/README.md) (datadog/datadog)

## How to use Datadog Helm repository

You need to add this repository to your Helm repositories:

```
helm repo add datadog https://helm.datadoghq.com
helm repo update
```
