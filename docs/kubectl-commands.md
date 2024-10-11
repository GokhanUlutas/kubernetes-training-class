# kubectl komutları

İşte temel **kubectl** komutlarının tablo formatında listesi:

| Kategori               | Komut                                  | Açıklama                                                              |
|------------------------|----------------------------------------|----------------------------------------------------------------------|
| **Genel**              | `kubectl version`                      | Kubectl ve sunucu sürümlerini gösterir.                              |
|                        | `kubectl get <resource>`               | Belirtilen kaynakların listesini gösterir (ör. pod, service, etc.).  |
|                        | `kubectl describe <resource> <name>`   | Kaynak hakkında ayrıntılı bilgi gösterir.                            |
|                        | `kubectl delete <resource> <name>`     | Belirtilen kaynağı siler.                                            |
|                        | `kubectl apply -f <filename>`          | YAML dosyasından kaynak oluşturur veya günceller.                    |
|                        | `kubectl create -f <filename>`         | YAML dosyasından yeni bir kaynak oluşturur.                          |
|                        | `kubectl edit <resource> <name>`       | Kaynağı düzenlemek için YAML dosyasını açar.                         |
|                        | `kubectl get all`                      | Tüm kaynakları listeler.                                             |
| **Pod Yönetimi**       | `kubectl get pods`                     | Tüm pod'ları listeler.                                               |
|                        | `kubectl logs <pod-name>`              | Belirtilen pod'un loglarını gösterir.                                |
|                        | `kubectl exec -it <pod-name> -- <cmd>` | Bir pod içinde komut çalıştırır.                                      |
|                        | `kubectl port-forward <pod-name> <port>`| Belirtilen pod'dan yerel bir porta yönlendirme yapar.                |
|                        | `kubectl delete pod <pod-name>`        | Belirtilen pod'u siler.                                              |
| **Deployment Yönetimi**| `kubectl get deployments`              | Deployment'ları listeler.                                            |
|                        | `kubectl rollout status deployment/<name>` | Deployment rollout durumunu gösterir.                               |
|                        | `kubectl rollout undo deployment/<name>` | Deployment'ı bir önceki sürüme geri alır.                            |
|                        | `kubectl scale deployment <name> --replicas=<count>` | Deployment için belirtilen sayıda replika ayarlar.                   |
| **Service ve Network** | `kubectl get services`                 | Servisleri listeler.                                                 |
|                        | `kubectl expose deployment <name> --type=NodePort --port=<port>` | Deployment için bir servis oluşturur.                                |
| **ConfigMap & Secret** | `kubectl get configmaps`               | ConfigMap'leri listeler.                                             |
|                        | `kubectl get secrets`                  | Secret'ları listeler.                                                |
|                        | `kubectl create configmap <name> --from-literal=<key>=<value>` | ConfigMap oluşturur.                                                 |
|                        | `kubectl create secret generic <name> --from-literal=<key>=<value>` | Generic bir Secret oluşturur.                                        |
| **Namespace Yönetimi** | `kubectl get namespaces`               | Namespace'leri listeler.                                             |
|                        | `kubectl create namespace <name>`      | Yeni bir namespace oluşturur.                                        |
|                        | `kubectl delete namespace <name>`      | Bir namespace'i siler.                                               |
| **Node Yönetimi**      | `kubectl get nodes`                    | Node'ları listeler.                                                  |
|                        | `kubectl cordon <node-name>`           | Bir node'u yeni pod planlaması için işaretler (cordon).               |
|                        | `kubectl drain <node-name>`            | Node'daki pod'ları tahliye eder (drain).                             |
|                        | `kubectl uncordon <node-name>`         | Node'u tekrar yeni pod planlaması için uygun hale getirir.            |
| **Diğer**              | `kubectl top node`                     | Node'lar için kaynak kullanımını gösterir.                           |
|                        | `kubectl top pod`                      | Pod'lar için kaynak kullanımını gösterir.                            |

Bu tablo, Kubernetes'deki temel yönetim görevlerini gerçekleştirmek için kullanılan en yaygın **kubectl** komutlarını listeler.


Kubernetes'te **aktif (geçerli) namespace**'i sorgulamak için aşağıdaki `kubectl` komutunu kullanabilirsiniz:

```bash
kubectl config view --minify --output 'jsonpath={..namespace}'
```

Bu komut, şu anda kullanılan aktif namespace'in adını döndürür. Eğer aktif bir namespace ayarlanmadıysa, varsayılan olarak **default** namespace'i kullanılır.

### Diğer Yöntem:
Alternatif olarak, geçerli context bilgilerini kontrol etmek için şu komutu kullanabilirsiniz:

```bash
kubectl config get-contexts $(kubectl config current-context)
```

Bu komut, mevcut context ve ona bağlı namespace dahil olmak üzere daha fazla ayrıntı sağlar.

### testt

