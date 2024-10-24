## Minikube üzerinde kubectl pod komutları

## minikube de pod ları listeleme

```bash
$ kubectl get pods -o wide -A
NAMESPACE     NAME                               READY   STATUS    RESTARTS      AGE   IP             NODE       NOMINATED NODE   READINESS GATES
kube-system   coredns-6f6b679f8f-lvhkj           1/1     Running   0             63m   10.244.0.2     minikube   <none>           <none>
kube-system   etcd-minikube                      1/1     Running   0             63m   192.168.49.2   minikube   <none>           <none>
kube-system   kube-apiserver-minikube            1/1     Running   0             63m   192.168.49.2   minikube   <none>           <none>
kube-system   kube-controller-manager-minikube   1/1     Running   0             63m   192.168.49.2   minikube   <none>           <none>
kube-system   kube-proxy-x8r4c                   1/1     Running   0             63m   192.168.49.2   minikube   <none>           <none>
kube-system   kube-scheduler-minikube            1/1     Running   0             63m   192.168.49.2   minikube   <none>           <none>
kube-system   storage-provisioner                1/1     Running   1 (63m ago)   63m   192.168.49.2   minikube   <none>           <none>
```

##