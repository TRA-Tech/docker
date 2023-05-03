
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
Docker, birçok farklı platformda çalışabilir ve uygulamaları hızlı ve güvenli bir şekilde dağıtmak için yaygın olarak kullanılır. Uygulamaların taşınabilirliğini artırırken, uygulama geliştiricileri ve sistem yöneticileri arasındaki işbirliğini kolaylaştırır.

 Docker'ın çalışma mantığı şu şekildedir:

**1. Docker Image Oluşturma:** Docker uygulaması, uygulamanın çalıştırılacağı işletim sistemi ve uygulamanın gereksinimleri dahil olmak üzere bir "docker image" oluşturmak için kullanılır. Docker Image, uygulamanın çalıştırılması için gerekli tüm bileşenleri içeren bir sanal ortamdır.

**2. Docker Container Oluşturma:** Docker Image, Docker Container'ın temelini oluşturur. Docker Container, Docker Image'ı çalıştırmak için kullanılır ve çalıştırıldığı cihaza veya sunucuya özgü herhangi bir konfigürasyona ihtiyaç duymaz. Docker Image'ın bir kopyası olarak düşünülebilir ve her bir Docker Container birbirinden izole edilmiştir.

**3. Docker Hub:** Docker Hub, Docker Image'ların bulunduğu bir merkezdir. Kullanıcılar, Docker Hub'da bulunan hazır Docker Image'ları kullanarak kendi Docker Container'larını kolayca oluşturabilirler. Ayrıca, kullanıcılar kendi oluşturdukları Docker Image'ları da Docker Hub'a yükleyebilir ve diğer kullanıcılarla paylaşabilirler.

**4. Dockerfile:** Dockerfile, Docker Image'ların nasıl oluşturulacağını belirleyen bir metin dosyasıdır. Kullanıcılar Dockerfile'ı kullanarak kendi özelleştirilmiş Docker Image'larını oluşturabilirler.

**5. Docker Compose:** Docker Compose, birden fazla Docker Container'ın bir arada çalıştığı karmaşık uygulamaların yönetimini kolaylaştırır. Docker Compose, Docker Image'larına, Docker Container'larına ve Docker ağlarına erişerek, uygulamanın bütününü yönetir.

**6. Docker Ağları:** Docker Ağları, Docker Container'larının birbirleriyle iletişim kurmasını sağlar. Ayrıca, Docker Container'ların belirli bir ağ arayüzüne bağlanmasına veya ağ arayüzünden çıkmasına izin verir.

Docker'ın çalışma mantığı, uygulamaların hızlı bir şekilde geliştirilmesi, test edilmesi ve dağıtılması için gereken temel araçları sağlar. Docker, uygulamaların taşınabilirliğini arttırır ve farklı cihazlar arasında sorunsuz bir şekilde çalışmasını sağlar.

Sonuç olarak, Docker, uygulama geliştirme ve dağıtım süreçlerinde büyük bir fark yaratan güçlü bir platformdur.

Docker teknolojisinden önce, uygulama geliştirme ve dağıtımı için sanal makineler (virtual machines - VMs) kullanılıyordu. Sanal makineler, bir fiziksel bilgisayarda çalışan bir işletim sistemine benzer bir sanal işletim sistemi çalıştıran, uygulama ve kaynakları birlikte paketleyen bir sanal ortam sağlarlar. Bu şekilde, uygulama geliştiricileri ve sistem yöneticileri, uygulamaların farklı bilgisayarlarda ve işletim sistemlerinde sorunsuz bir şekilde çalışmasını sağlayabilirler.

Ancak, sanal makinelerin kullanımı bazı dezavantajlar da taşır. Sanal makineler, daha fazla bellek ve işlemci gücü gerektirdiğinden daha yavaş performans gösterirler. Ayrıca, sanal makinelerin ölçeklendirilmesi zor ve yavaş olabilir. Bu nedenle, Docker teknolojisi, sanal makinelerin yerini alarak daha hafif ve hızlı bir alternatif sunar. 

Sanal mimari ve Konteyner mimarisinin farkları aşağıdaki gibidir.

![image](https://user-images.githubusercontent.com/100773960/228242016-c8b49f09-4a89-45ac-b1f1-b7595010c06a.png)


<br>

##


<img src="https://user-images.githubusercontent.com/100773960/231446433-cee44a61-4804-47e8-991d-a0d8cae53eff.png" width="650" height="300">

Play with Docker (PWD), Docker teknolojilerini öğrenmek için kullanıcıların kullanabileceği bir çevrimiçi laboratuvardır. Bu platform, Docker'ın özelliklerini keşfetmek, Docker komutlarını öğrenmek ve uygulamaları Docker üzerinde uygulama çalıştırmak isteyenler için kullanımı kolay bir platformdur.

Play with Docker, kullanıcılara bir Docker çevrimiçi laboratuvarı sunar. Kullanıcılar, tarayıcılarında bir Docker çevresi çalıştırarak, Docker hub üzerindeki imajları indirip, imajlarla çalışabilirler. Platform ayrıca, Docker CLI'yi kullanarak komut satırından çalıştırmak için bir terminal sunar.

Play with Docker, Docker üzerinde uygulamaları çalıştırmak ve Docker ile ilgili konuları öğrenmek için kullanabileceğiniz birçok örnek uygulama sunar. Kullanıcılar, bu uygulamaları çalıştırarak Docker'ın nasıl çalıştığını, Docker konteynerlerinin nasıl oluşturulduğunu ve nasıl yönetildiğini öğrenebilirler.

Play with Docker, Dockerhub üzerinden hesap açılarak kullanılabilir ve tamamen ücretsizdir. Kullanıcılar, platformu ziyaret ederek hemen Docker özelliklerini keşfetmeye başlayabilirler. Play with Docker, Docker'ın özelliklerini öğrenmek ve Docker'ın nasıl çalıştığı hakkında deneyim kazanmak isteyenler için harika bir kaynak ve eğitim platformudur.

PWD platformuna https://labs.play-with-docker.com/ adresinden erişebilirsiniz. Sitenin ana sayfasında, Docker imajları ve örnek uygulamalarla birlikte kullanım için birçok kaynak ve öğretici yer alır.
## 
<br>

## Docker Bileşenleri


Docker Engine, Docker'ın temel bileşenidir ve uygulamaların Docker konteynerleri içinde çalıştırılmasını sağlayan bir açık kaynaklı konteyner çalıştırma motorudur. İşletim sistemi düzeyinde sanallaştırma teknolojisi kullanır ve birden fazla konteynerin aynı işletim sistemi çekirdeği üzerinde çalışmasına olanak tanır.

Docker Engine, birçok bileşeni içerir. Bunlar arasında Docker Daemon, Docker API, Docker CLI, Docker imajları ve Docker registry yer alır.

- **Docker Daemon**, Docker Engine'in kalbidir. Konteynerleri yönetir, imajları indirir ve saklar, ağları oluşturur ve yönetir, sistem kaynaklarını konteynerler arasında paylaştırır ve diğer Docker bileşenleriyle iletişim kurar.
- **Docker API**, uygulamaların Docker Engine'e erişmesine olanak tanır. Docker CLI gibi araçlar, Docker API'ye istek gönderir ve konteynerlerin, imajların ve diğer kaynakların yönetimini sağlar.
- **Docker CLI**, kullanıcıların Docker Engine ile etkileşim kurmalarını sağlar. Kullanıcılar, konteynerlerin, imajların ve diğer Docker kaynaklarının oluşturulmasını, yönetilmesini ve silinmesini sağlayabilirler.
- **Docker imajları**, konteynerlerin temel yapı taşıdır. İmajlar, bir uygulama ve bağımlılıklarını içerir ve konteynerlerin oluşturulmasında kullanılır.
- **Docker registry**, Docker imajlarının depolanmasını ve paylaşılmasını sağlar. Docker Hub, Docker'ın varsayılan imaj deposudur ancak farkı registry sunucuları da özelleştirilerek kullanılabilir.

Docker Engine, birçok platformda çalışabilir ve birçok programlama dili ve araç setiyle uyumlu olabilir. Bu nedenle uygulamaların hızlı ve güvenli bir şekilde dağıtılması için yaygın olarak kullanılan bir teknolojidir.

## Docker Container


Container teknolojisi, yazılım uygulamalarını izole edilmiş bir çalışma ortamında çalıştırmak için kullanılan bir sanallaştırma yöntemidir. Containerlar, uygulamaların çalışması için gerekli olan tüm dosyaları, bağımlılıkları ve yapılandırmaları bir arada tutan taşınabilir bir paketleme formatıdır.

![container](https://user-images.githubusercontent.com/100773960/228242830-2d2c4a56-29cf-473d-a1dc-c67199955789.jpeg)

Bu teknoloji, uygulamaların farklı ortamlarda çalışmasını kolaylaştırır ve taşınabilir hale getirir. Herhangi bir sistemdeki container uygulamaları, sistemdeki diğer uygulamaları etkilemeden çalıştırılabilir.
Container teknolojisi, çeşitli avantajlar sağlar. Örneğin, daha yüksek işletim sistemi yoğunluğu sağlar, daha hızlı uygulama dağıtımı için kullanılabilir, uygulama izolasyonunu sağlar ve daha az donanım kaynağı gerektirir. En popüler container teknolojileri arasında **Docker**, Kubernetes ve Apache Mesos bulunur.


