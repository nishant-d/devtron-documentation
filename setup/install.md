# Install Devton

## Install with Helm

Devtron Helm chart is available at

https://github.com/devtron-labs/devtron-installation-script/tree/main/charts 

***To Install Run following command***

```bash
$ git clone https://github.com/devtron-labs/devtron-installation-script.git
$ cd devtron-installation-script/charts
$ #modify values in values.yaml
$ helm install devtron . -f values.yaml

```

## Install with kubectl

If you just want to use kubectl to install Devtron platform, then please follow following steps:

```bash
$ git clone [https://github.com/devtron-labs/devtron-installation-script.git](https://github.com/devtron-labs/devtron-installation-script.git)
$ cd devtron-installation-script/charts/template
$ kubectl apply -n devtroncd -f charts/template/install.yaml
$ # wait for it to finish
$ #edit charts/template/configmap-secret.yaml
$ kubectl apply -n devtroncd -f charts/template/configmap-secret.yaml
$ kubectl apply -n devtroncd -f charts/template/devtron-installer.yaml

```

## Access Devtron dashboard

Devtron dashboard in now available at the `BASE_URL/dashboard`, where `BASE_URL` is 
- same as provided in `values.yaml` in case of installation via helm chart 
- provided in `charts/template/configmap-secret.yaml` in case of installation via kubectl.

For login use username:`admin` and for password run command mentioned below.

```bash
$ kubectl -n devtroncd get secret devtron-secret -o jsonpath='{.data.ACD_PASSWORD}' | base64 -d
```

### Configuration

All parameters mentioned in the `values.yaml` are mandatory.

**First section is ***secrets.env*** and it has following properties**

| Parameter | Description | Default |
|:----------|:------------|:--------|
| POSTGRESQL_PASSWORD | password for postgres database (required) | change-me |
| GIT_TOKEN | git token for the gitops work flow, please note this is not for source code of repo and this token should have full access to create, delete, update repository (required) |  |
| WEBHOOK_TOKEN | If you want to continue using jenkins for CI then please provide this for authentication of requests (optional)  |  |


<br><br>

**Second section is ***configs*** and has following properties**

<br>

| Parameter | Description | Default |
|:----------|:------------|:--------|
| BASE_URL_SCHEME | either of http or https | http |
| BASE_URL | url without scheme and trailing slash (required) `eg. devtron.ai` | `change-me` |
| DEX_CONFIG | dex config if you want to integrate login with SSO (optional) for more information check [Argocd documentation](https://argoproj.github.io/argo-cd/operator-manual/user-management/) | 
| GIT_PROVIDER | git provider for storing config files for gitops, currently only GITHUB and GITLAB are supported | `GITHUB` | |
| GITLAB_NAMESPACE_ID | if GIT_PROVIDER is GITLAB | | 
| GITLAB_NAMESPACE_NAME | if GIT_PROVIDER is GITLAB | |
| GIT_USERNAME | git username for the GIT_PROVIDER | |
| GITHUB_ORGANIZATION | if GIT_PROVIDER is GITHUB | |
| DEFAULT_CD_LOGS_BUCKET_REGION | AWS region of bucket to store CD logs | |
| DEFAULT_CACHE_BUCKET | AWS bucket to store docker cache |  |
| DEFAULT_CACHE_BUCKET_REGION | AWS region of cache bucket defined in previous step | |
| DEFAULT_BUILD_LOGS_BUCKET | AWS bucket to store build logs | |
| CHARTMUSEUM_STORAGE_AMAZON_BUCKET | AWS bucket to store charts |  |
| CHARTMUSEUM_STORAGE_AMAZON_REGION | AWS region for bucket defined in previous step to store charts | |
| EXTERNAL_SECRET_AMAZON_REGION | AWS region for secret manager to pick |  |
| PROMETHEUS_URL | url of prometheus where all cluster data is stored, if this is wrong, you will not be able to see application metrics like cpu, ram, http status code, latency and throughput |  |

<br>

example of DEX_CONFIG is

    DEX_CONFIG: |-
      connectors:
        - type: oidc
          id: google
          name: Google
          config:
            issuer: https://accounts.google.com
            clientID: xxxxxxxx-qwwdsdsqsxxxxxxxxx.apps.googleusercontent.com
            clientSecret: fssdsdw121wwxssd
            redirectURI: <BASE_URL_SCHEME>://<BASE_URL>/api/dex/callback
            hostedDomains:
            - abc.com

**Please Note:**
Ensure that the cluster has access to the DEFAULT_CACHE_BUCKET, DEFAULT_BUILD_LOGS_BUCKET, CHARTMUSEUM_STORAGE_AMAZON_BUCKET and AWS secrets backends (SSM & secrets manager)
