kustomize build common/cert-manager/cert-manager/base | kubectl apply -f -
kustomize build common/cert-manager/kubeflow-issuer/base | kubectl apply -f -

kustomize build common/istio-1-9/istio-crds/base | kubectl apply -f -
kustomize build common/istio-1-9/istio-namespace/base | kubectl apply -f -
kustomize build common/istio-1-9/istio-install/base | kubectl apply -f -


kustomize build common/dex/overlays/istio | kubectl apply -f -

kustomize build common/oidc-authservice/base | kubectl apply -f -

kustomize build common/knative/knative-serving/base | kubectl apply -f -
kustomize build common/istio-1-9/cluster-local-gateway/base | kubectl apply -f -

kustomize build common/knative/knative-eventing/base | kubectl apply -f -

kustomize build common/kubeflow-namespace/base | kubectl apply -f -

kustomize build common/kubeflow-roles/base | kubectl apply -f -

kustomize build common/istio-1-9/kubeflow-istio-resources/base | kubectl apply -f -


kustomize build apps/pipeline/upstream/env/platform-agnostic-multi-user | kubectl apply -f -

kustomize build apps/kfserving/upstream/overlays/kubeflow | kubectl apply -f -


kustomize build apps/katib/upstream/installs/katib-with-kubeflow | kubectl apply -f -

kustomize build apps/centraldashboard/upstream/overlays/istio | kubectl apply -f -


kustomize build apps/admission-webhook/upstream/overlays/cert-manager | kubectl apply -f -


kustomize build apps/jupyter/notebook-controller/upstream/overlays/kubeflow | kubectl apply -f -


kustomize build apps/jupyter/jupyter-web-app/upstream/overlays/istio | kubectl apply -f -


kustomize build apps/profiles/upstream/overlays/kubeflow | kubectl apply -f -


kustomize build apps/volumes-web-app/upstream/overlays/istio | kubectl apply -f -


kustomize build apps/tensorboard/tensorboards-web-app/upstream/overlays/istio | kubectl apply -f -


kustomize build apps/tensorboard/tensorboard-controller/upstream/overlays/kubeflow | kubectl apply -f -


kustomize build apps/training-operator/upstream/overlays/kubeflow | kubectl apply -f -


kustomize build apps/mpi-job/upstream/overlays/kubeflow | kubectl apply -f -


kustomize build common/user-namespace/base | kubectl apply -f -


-------------------------------------------------------------------------------------------------------------------------------

kustomize build common/cert-manager/cert-manager/base > argo-demo/cert-manager.yaml
kustomize build common/cert-manager/kubeflow-issuer/base > argo-demo/kubeflow-issuer.yaml

kustomize build common/istio-1-9/istio-crds/base > argo-demo/istio-crds.yaml
kustomize build common/istio-1-9/istio-namespace/base > argo-demo/istio-namespace
kustomize build common/istio-1-9/istio-install/base > argo-demo/istio-install.yaml


kustomize build common/dex/overlays/istio > argo-demo/dex.yaml

kustomize build common/oidc-authservice/base > argo-demo/oidc-authservice.yaml

kustomize build common/knative/knative-serving/base > argo-demo/knative-serving.yaml
kustomize build common/istio-1-9/cluster-local-gateway/base > argo-demo/cluster-local-gateway.yaml

kustomize build common/knative/knative-eventing/base > argo-demo/knative-eventing.yaml

kustomize build common/kubeflow-namespace/base > argo-demo/kubeflow-namespace.yaml

kustomize build common/kubeflow-roles/base > argo-demo/kubeflow-roles.yaml

kustomize build common/istio-1-9/kubeflow-istio-resources/base > argo-demo/kubeflow-istio-resources.yaml


kustomize build apps/pipeline/upstream/env/platform-agnostic-multi-user > argo-demo/kubeflow-pipelines.yaml

kustomize build apps/kfserving/upstream/overlays/kubeflow > argo-demo/kfserving.yaml


kustomize build apps/katib/upstream/installs/katib-with-kubeflow > argo-demo/katib-with-kubeflow.yaml

kustomize build apps/centraldashboard/upstream/overlays/istio > argo-demo/centraldashboard.yaml


kustomize build apps/admission-webhook/upstream/overlays/cert-manager > argo-demo/admission-webhook-cert-manager.yaml


kustomize build apps/jupyter/notebook-controller/upstream/overlays/kubeflow > argo-demo/notebook-controller.yaml


kustomize build apps/jupyter/jupyter-web-app/upstream/overlays/istio > argo-demo/jupyter-web-app.yaml


kustomize build apps/profiles/upstream/overlays/kubeflow > argo-demo/jupyter-web-app.yaml



kustomize build apps/volumes-web-app/upstream/overlays/istio > argo-demo/volumes-web-app.yaml


kustomize build apps/tensorboard/tensorboards-web-app/upstream/overlays/istio > argo-demo/tensorboards-web-app.yaml


kustomize build apps/tensorboard/tensorboard-controller/upstream/overlays/kubeflow > argo-demo/tensorboard-controller.yaml


kustomize build apps/training-operator/upstream/overlays/kubeflow > argo-demo/training-operator.yaml


kustomize build apps/mpi-job/upstream/overlays/kubeflow > argo-demo/mpi-job.yaml


kustomize build common/user-namespace/base > argo-demo/user-namespace.yaml
