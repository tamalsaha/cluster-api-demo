# cluster-api-docker

```
$ clusterctl init --infrastructure docker
                                        
Fetching providers
Installing cert-manager Version="v0.16.1"
Waiting for cert-manager to be available...
Installing Provider="cluster-api" Version="v0.3.14" TargetNamespace="capi-system"
Installing Provider="bootstrap-kubeadm" Version="v0.3.14" TargetNamespace="capi-kubeadm-bootstrap-system"
Installing Provider="control-plane-kubeadm" Version="v0.3.14" TargetNamespace="capi-kubeadm-control-plane-system"
Installing Provider="infrastructure-docker" Version="v0.3.14" TargetNamespace="capd-system"

Your management cluster has been initialized successfully!

You can now create your first workload cluster by running the following:

  clusterctl config cluster [name] --kubernetes-version [version] | kubectl apply -f -
```


```
$ kubectl get pods --all-namespaces
NAMESPACE                           NAME                                                             READY   STATUS    RESTARTS   AGE
capd-system                         capd-controller-manager-8594dfd47d-tftbx                         2/2     Running   0          83s

capi-kubeadm-bootstrap-system       capi-kubeadm-bootstrap-controller-manager-ddcc95784-t46n9        2/2     Running   0          89s

capi-kubeadm-control-plane-system   capi-kubeadm-control-plane-controller-manager-d85dfd44c-szmvg    2/2     Running   0          86s

capi-system                         capi-controller-manager-5cd969bf55-pnql6                         2/2     Running   0          92s

capi-webhook-system                 capi-controller-manager-68c9ff8646-v55zd                         2/2     Running   0          93s
capi-webhook-system                 capi-kubeadm-bootstrap-controller-manager-7cf85756c5-mxkfr       2/2     Running   0          91s
capi-webhook-system                 capi-kubeadm-control-plane-controller-manager-7854964ff4-5vbgj   2/2     Running   0          88s

cert-manager                        cert-manager-cainjector-fc6c787db-6hlpc                          1/1     Running   0          2m28s
cert-manager                        cert-manager-d994d94d7-z68jd                                     1/1     Running   0          2m28s
cert-manager                        cert-manager-webhook-845d9df8bf-qbnhj                            1/1     Running   0          2m28s
```


clusterctl config cluster capi-quickstart --flavor development \
  --kubernetes-version v1.19.7 \
  --control-plane-machine-count=3 \
  --worker-machine-count=3 \
  > capi-quickstart.yaml
  