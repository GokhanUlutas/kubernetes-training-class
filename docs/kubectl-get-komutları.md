## kubectl get komutları

```bash
@ulutasgo ➜ /workspaces/kubernetes-training-class (main) $ kubectl get nodes
NAME       STATUS   ROLES           AGE   VERSION
minikube   Ready    control-plane   90m   v1.31.0

@ulutasgo ➜ /workspaces/kubernetes-training-class (main) $ kubectl get namespaces
NAME              STATUS   AGE
default           Active   91m
kube-node-lease   Active   91m
kube-public       Active   91m
kube-system       Active   91m

@ulutasgo ➜ /workspaces/kubernetes-training-class (main) $ kubectl get services
NAME         TYPE        CLUSTER-IP   EXTERNAL-IP   PORT(S)   AGE
kubernetes   ClusterIP   10.96.0.1    <none>        443/TCP   91m

@ulutasgo ➜ /workspaces/kubernetes-training-class (main) $ kubectl get deployments
No resources found in default namespace.

@ulutasgo ➜ /workspaces/kubernetes-training-class (main) $ kubectl get deployments -n kube-system
NAME      READY   UP-TO-DATE   AVAILABLE   AGE
coredns   1/1     1            1           91m

@ulutasgo ➜ /workspaces/kubernetes-training-class (main) $ kubectl get daemonset -n kube-system
NAME         DESIRED   CURRENT   READY   UP-TO-DATE   AVAILABLE   NODE SELECTOR            AGE
kube-proxy   1         1         1       1            1           kubernetes.io/os=linux   92m
```