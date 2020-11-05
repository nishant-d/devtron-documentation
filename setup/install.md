# Install Devton

## Install with Helm

Devtron Helm chart is available at

https://github.com/devtron-labs/devtron-installation-script/tree/main/charts

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

