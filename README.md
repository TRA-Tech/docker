
# Docker 
## İçindekiler
- [Docker Swarm](https://github.com/TRA-Tech/docker/blob/main/docker-swarm.md)
- [Docker Compose](https://github.com/TRA-Tech/docker/blob/main/docker-compose.md) 
- [Docker Volume](https://github.com/TRA-Tech/docker/blob/main/docker-volume.md)
- [Docker Registry](https://github.com/TRA-Tech/docker/blob/main/docker-registry.md)
- [Dockerfile](https://github.com/TRA-Tech/docker/blob/main/Dockerfile.md)


![image](https://user-images.githubusercontent.com/100773960/228240739-661990d7-be4e-4e52-a273-8f9c44f2519e.png)

Docker, uygulamaların taşınabilirliğini sağlayan ve yazılım geliştirme sürecini hızlandıran bir konteyner platformudur. 

Docker, açık kaynaklı bir platform olması nedeniyle, geniş bir topluluk tarafından desteklenmektedir ve sürekli olarak geliştirilmektedir. Docker, hızlı ve kolay bir şekilde uygulama oluşturmanızı, dağıtmanızı ve yönetmenizi sağlar.
Ayrıca, Docker Hub gibi birçok farklı kaynak, hazır konteyner görüntüleri ve konfigürasyon dosyaları sunarak, uygulama geliştirme ve dağıtım sürecini hızlandırır.
Docker, birçok farklı platformda çalışabilir ve uygulamaları hızlı ve güvenli bir şekilde dağıtmak için yaygın olarak kullanılır. Docker, uygulamaların taşınabilirliğini artırırken, uygulama geliştiricileri ve sistem yöneticileri arasındaki işbirliğini kolaylaştırır.

Sonuç olarak, Docker, uygulama geliştirme ve dağıtım süreçlerinde büyük bir fark yaratan güçlü bir platformdur.

Docker teknolojisinden önce, uygulama geliştirme ve dağıtımı için sanal makineler (virtual machines - VMs) kullanılıyordu. Sanal makineler, bir fiziksel bilgisayarda çalışan bir işletim sistemine benzer bir sanal işletim sistemi çalıştıran ve uygulama ve kaynakları birlikte paketleyen bir sanal ortam sağlarlar. Bu şekilde, uygulama geliştiricileri ve sistem yöneticileri, uygulamaların farklı bilgisayarlarda ve işletim sistemlerinde sorunsuz bir şekilde çalışmasını sağlayabilirler.

Ancak, sanal makinelerin kullanımı bazı dezavantajlar da taşır. Sanal makineler, daha fazla bellek ve işlemci gücü gerektirdiğinden daha yavaş performans gösterirler. Ayrıca, sanal makinelerin ölçeklendirilmesi zor ve yavaş olabilir. Bu nedenle, Docker teknolojisi, sanal makinelerin yerini alarak daha hafif ve hızlı bir alternatif sunar. 

Sanal mimari ve Konteyner mimarisinin farkları aşağıdaki gibidir.

![image](https://user-images.githubusercontent.com/100773960/228242016-c8b49f09-4a89-45ac-b1f1-b7595010c06a.png)


## Docker Bileşenleri


Docker Engine, Docker'ın temel bileşenidir ve uygulamaların Docker konteynerleri içinde çalıştırılmasını sağlayan bir açık kaynaklı konteyner çalıştırma motorudur. Docker Engine, işletim sistemi düzeyinde sanallaştırma teknolojisi kullanır ve birden fazla konteynerin aynı işletim sistemi çekirdeği üzerinde çalışmasına olanak tanır.

Docker Engine, birçok bileşeni içerir. Bunlar arasında Docker Daemon, Docker API, Docker CLI, Docker imajları ve Docker registry yer alır.

- **Docker Daemon**, Docker Engine'in kalbidir. Konteynerleri yönetir, imajları indirir ve saklar, ağları oluşturur ve yönetir, sistem kaynaklarını konteynerler arasında paylaştırır ve diğer Docker bileşenleriyle iletişim kurar.
- **Docker API**, uygulamaların Docker Engine'e erişmesine olanak tanır. Docker CLI gibi araçlar, Docker API'ye istek gönderir ve konteynerlerin, imajların ve diğer kaynakların yönetimini sağlar.
- **Docker CLI**, kullanıcıların Docker Engine ile etkileşim kurmalarını sağlar. Kullanıcılar, konteynerlerin, imajların ve diğer Docker kaynaklarının oluşturulmasını, yönetilmesini ve silinmesini sağlayabilirler.
- **Docker imajları**, konteynerlerin temel yapı taşıdır. İmajlar, bir uygulama ve bağımlılıklarını içerir ve konteynerlerin oluşturulmasında kullanılır.
- **Docker registry**, Docker imajlarının depolanmasını ve paylaşılmasını sağlar. Docker Hub, Docker'ın varsayılan imaj deposudur ancak farkı registry sunucuları da özelleştirilerek kullanılabilir.

Docker Engine, birçok platformda çalışabilir ve birçok programlama dili ve araç setiyle uyumlu olabilir. Bu nedenle, Docker Engine, uygulamaların hızlı ve güvenli bir şekilde dağıtılması için yaygın olarak kullanılan bir teknolojidir.

## Docker Container


Container teknolojisi, yazılım uygulamalarını izole edilmiş bir çalışma ortamında çalıştırmak için kullanılan bir sanallaştırma yöntemidir. Containerlar, uygulamaların çalışması için gerekli olan tüm dosyaları, bağımlılıkları ve yapılandırmaları bir arada tutan taşınabilir bir paketleme formatıdır.

![container](https://user-images.githubusercontent.com/100773960/228242830-2d2c4a56-29cf-473d-a1dc-c67199955789.jpeg)

Bu teknoloji, uygulamaların farklı ortamlarda çalışmasını kolaylaştırır ve taşınabilir hale getirir. Herhangi bir sistemdeki container uygulamaları, sistemdeki diğer uygulamaları etkilemeden çalıştırılabilir.
Container teknolojisi, çeşitli avantajlar sağlar. Örneğin, daha yüksek işletim sistemi yoğunluğu sağlar, daha hızlı uygulama dağıtımı için kullanılabilir, uygulama izolasyonunu sağlar ve daha az donanım kaynağı gerektirir. En popüler container teknolojileri arasında **Docker**, Kubernetes ve Apache Mesos bulunur.


