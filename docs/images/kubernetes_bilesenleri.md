## Kubernetes bileşenleri

Açıklamalar:

Kubectl (Kullanıcı): Kubernetes kullanıcısı veya yönetici, cluster üzerinde işlem yapmak için kubectl aracını kullanır.

API Server: Kubernetes API sunucusu, tüm bileşenlerin birbiriyle iletişimini sağlar.

etcd: Cluster bilgilerini tutan veritabanıdır.

Scheduler: Yeni pod'ların hangi node üzerinde çalışacağını belirler.

Controller Manager: Kubernetes'teki çeşitli denetleyicileri çalıştırır.

Kubelet: Her node'da çalışan ajan olup, pod'ların çalışmasını yönetir.

Kube-Proxy: Ağ trafiğini yönlendirir ve servisler arası iletişimi sağlar.

Container Runtime: Pod'lardaki konteynerleri çalıştıran altyapıdır (Docker, containerd vb.).
