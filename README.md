# fleet-infra
Requirements: Docker Desktop (enable Kubernetes)

https://docs.gitops.weave.works/docs/next/open-source/getting-started/install-OSS/

flux bootstrap github \
  --token-auth \
  --owner=nbelhumeur \
  --repository=fleet-infra \
  --branch=main \
  --path=clusters/my-cluster \
  --personal \
  --components-extra image-reflector-controller,image-automation-controller

gitops create dashboard ww-gitops \
  --password= \
  --export > ./clusters/my-cluster/weave-gitops-dashboard.yaml

