# monolith-gitlab-k8s

BhZ0h2sRm6/tHBZzNoQamr074LgGU2msaKmUrXICdTQ=
This project is intended as a **template** to those who want to deploy Gitlab-CE to Kubernetes without using the Helm chart. 

Since this is a template, it might not suit your production needs. You will certainly need to edit it.

### Quickstart

* Clone the project.
* Run `kubectl apply -f ./monolith-gitlab-k8s/k8s`

### Gotchas

* The deployment runs 1 replica.
* The PVCs will use the default storage class, you need to have a proper one set.
* The service will expose 80(HTTP), 443(HTTPS) and 22 (SSH) ports, maybe you won't need them all, don't hesitate to edit it.
* The Gitlab image tag is set to `latest`, this is not recommended in production. Replace it with the explicit version from https://hub.docker.com/r/gitlab/gitlab-ce/tags.
* This deployment doesn't have container resource limits. It could starve other processes on your nodes.
 