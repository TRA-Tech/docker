## Docker Swarm

<img src="https://user-images.githubusercontent.com/100773960/228243346-090fc49b-463d-4bfa-9f46-937dff5214ab.png" width="500" height="300">


Docker Swarm, Docker motoru üzerinde birden fazla makine üzerinde Docker konteynerlarının yönetimini ve dağıtımını sağlayan bir araçtır. Swarm, yüksek kullanılabilirlik, ölçeklenebilirlik ve daha iyi güvenilirlik sağlar. Aşağıda Swarm'ın kullanımı için genel adımlar verilmiştir:

1. Swarm kümesi oluşturma: Swarm kümesi, birden fazla Docker makinesinden oluşur ve bu makineler arasında iletişim kurmak için Swarm yöneticisi kullanır. Swarm yöneticisi, Docker makinesi olarak yapılandırılmış bir ana bilgisayarda çalıştırılır. Swarm kümesi oluşturmak için aşağıdaki komutu kullanabilirsiniz:
```
docker swarm init
```

2. Node'ların eklenmesi: Swarm kümesine node'lar eklenerek, Docker konteynerları Swarm kümesinde dağıtılabilir. Node'lar, Swarm yöneticisi tarafından yönetilir ve bunlar Swarm kümesindeki Docker konteynerlarının çalıştırıldığı yerlerdir. Node'ları Swarm kümesine eklemek için aşağıdaki komutu kullanabilirsiniz:
```
docker swarm join --token <join_token> <manager_node_ip>:<port>
```

3. Servislerin oluşturulması: Swarm kümesinde çalışacak Docker servislerini oluşturabilirsiniz. Bir servis, Swarm kümesinde belirli bir sayıda konteynerı çalıştırmak için kullanılır. Servisleri oluşturmak için aşağıdaki komutu kullanabilirsiniz:
```
docker service create --name <service_name> --replicas <replica_count> <image>
```

4. Servisleri güncelleme: Servisleri güncellemek ve yeni Docker imajları yüklemek istediğinizde, servisleri güncellemek için aşağıdaki komutu kullanabilirsiniz:
```
docker service update <service_name> --image <new_image_name>
```

5. Kontrol ve yönetim: Docker Swarm'ın sağladığı kontrol ve yönetim araçlarını kullanarak, Swarm kümenizdeki servislerin durumunu, sağlığını ve performansını izleyebilirsiniz. Örneğin, aşağıdaki komutla Swarm kümesindeki servislerin durumunu görüntüleyebilirsiniz:
```
docker service ls
```

Docker Swarm, birden fazla Docker makinesi arasında Docker konteynerları yönetmek için güçlü bir araçtır. Bu adımları izleyerek, Docker Swarm kümenizi oluşturabilir, yönetebilir ve kontrol edebilirsiniz.
<br>
