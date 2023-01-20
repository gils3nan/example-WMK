# example-WMK

#### Prerequisites
- [Install and Set Up kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Install and Set Up minikube](https://minikube.sigs.k8s.io/docs/start/)
- [ArgoCD Getting started](https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd)

#### Guide

Commands to set up the `demo-wmk-app` application running on the same cluster as ArgoCD (local)

1. Clone this repo
2. Move to the root of the repo
3. Run `kubectl apply -f application.yml`
4. Wait for confirmation of application configuration
5. Check that the application appears in your ArgoCD UI
6. To view the application site - Run `kubectl -n <NAMESPACE> get services <SERVICE-NAME>` to get the running ports.
7. Open a new tab in the terminal `to run the port forwading command `kubectl port-forward svc/<SERVICE-NAME> -n <NAMESPACE> <PORT-FORWORD-TO>:<PORT-FROM-PREVIOUS-STEP>`
8. In the browser navigate to `http://localhost:<PORT-FORWORD-TO>/` and set up the WP application.

#### References:
- [Kubernetes Example Applications](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)
