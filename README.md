# Argocd-exmaple-repo
This is where I practice argocd for GitOps. If you want to know official test code, refer to official websites below

> [Official ArgoCD Github repo](https://github.com/argoproj/argo-cd)    
> [Official ArgoCD web site](https://argo-cd.readthedocs.io/en/latest/)

## Used project
ArgoCD Sample project : Guestbook
* image : gcr.io/heptio-images/ks-guestbook-demo:0.2
* ex) Children of official Github examples (https://github.com/argoproj/argo-cd/tree/master/applicationset/examples)

## List
* ApplicationSet

## ArgoCD version

### NOTES
When install ArgoCD over v2.3, there is issue with argo-repo-controller about GPG. [refer to](https://github.com/argoproj/argo-cd/issues/11818)

> Fix the GPG problem with following in helm values.yml file:
```repoServer:
   containerSecurityContext:
     seccompProfile:
       type: Unconfined
```

### ArgoCD version
`$ argocd version`
```
argocd: v2.5.0+b895da4
  BuildDate: 2022-10-25T15:01:45Z
  GitCommit: b895da457791d56f01522796a8c3cd0f583d5d91
  GitTreeState: clean
  GoVersion: go1.18.7
  Compiler: gc
  Platform: darwin/amd64
argocd-server: v2.5.4+86b2dde
  BuildDate: 2022-12-06T19:46:25Z
  GitCommit: 86b2dde8e4bf1187acd2b4294e94451cd104dad8
  GitTreeState: clean
  GoVersion: go1.18.8
  Compiler: gc
  Platform: linux/amd64
  Kustomize Version: v4.5.7 2022-08-02T16:35:54Z
  Helm Version: v3.10.1+g9f88ccb
  Kubectl Version: v0.24.2
  Jsonnet Version: v0.18.0
```